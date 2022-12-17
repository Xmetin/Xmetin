# Import necessary libraries
import pygame
import random

# Initialize pygame
pygame.init()

# Set up the game window and background
window_size = (800, 600)
window = pygame.display.set_mode(window_size)
pygame.display.set_caption("The Lost City of Gold")
bg_color = (0, 0, 0)

# Set up the player character
player_image = pygame.image.load("player.png")
player_rect = player_image.get_rect()
player_rect.center = (400, 300)

# Set up the allied characters
maria_image = pygame.image.load("maria.png")
maria_rect = maria_image.get_rect()
maria_rect.center = (300, 300)

jack_image = pygame.image.load("jack.png")
jack_rect = jack_image.get_rect()
jack_rect.center = (500, 300)

sarah_image = pygame.image.load("sarah.png")
sarah_rect = sarah_image.get_rect()
sarah_rect.center = (600, 300)

# Set up the enemy characters
hector_image = pygame.image.load("hector.png")
hector_rect = hector_image.get_rect()
hector_rect.center = (700, 300)

jaguar_king_image = pygame.image.load("jaguar_king.png")
jaguar_king_rect = jaguar_king_image.get_rect()
jaguar_king_rect.center = (100, 300)

cultists_image = pygame.image.load("cultists.png")
cultists_rect = cultists_image.get_rect()
cultists_rect.center = (200, 300)

# Set up the treasure
treasure_image = pygame.image.load("treasure.png")
treasure_rect = treasure_image.get_rect()

# Set up the game clock
clock = pygame.time.Clock()

# Set up game variables
game_over = False
player_moved = False

# Main game loop
while not game_over:
    # Handle events
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            game_over = True
        elif event.type == pygame.KEYDOWN:
            if event.key == pygame.K_w:
                player_rect.y -= 10
                player_moved = True
            elif event.key == pygame.K_s:
                player_rect.y += 10
                player_moved = True
            elif event.key == pygame.K_a:
                player_rect.x -= 10
                player_moved = True
            elif event.key == pygame.K_d:
                player_rect.x += 10
                player_moved = True
    
    # Update game state
    if player_moved:
        if player_rect.coll

