#milestone 1: make the grid with the input (see screenshot in folder)
def milestone_1(tiles):
    list_of_tiles = tiles.split(",")
    p_size = int(len(list_of_tiles) ** 0.5)
    
    top_border = "┌" + "────┬" * (p_size - 1) + "────┐"
    print(top_border)
    
    for i in range(p_size):
        row_labels = ""
        for char in range(p_size):
            tile_label = list_of_tiles[i * p_size + char]
            if tile_label == "":
                tile_label = "    "
            elif int(tile_label) < 10:
                tile_label = "  " + tile_label + " "
            else: 
                tile_label = " " + tile_label + " "
            row_labels += "│" + tile_label 
        row_labels += "│"
        print(row_labels)
        
        if i != p_size - 1: 
            seperator = "├" + "────┼" * (p_size - 1) + "────┤"
            print(seperator)
            
    bottom_border = "└" + "────┴" * (p_size - 1) + "────┘"
    print(bottom_border)
#input
#milestone_1("1,2,3,4,5,6,7,8,9,10,,12,13,14,11,15")
#milestone_1("1,,2,3,4,5,6,7,8")
#milestone_1("1,2,3,4,5,6,7,8,9,10,,11,12,13,14,15,16,17,18,19,20,21,22,23,24")


#milestone 2: see screenshot in folder
# Printing the grid board
def milestone_1(tiles):
    list_of_tiles = tiles.split(",")
    puzzle_size = int(len(list_of_tiles) ** 0.5)

    # Printing the top border of the grid
    top_border = "┌" + "────┬" * (puzzle_size - 1) + "────┐"
    print(top_border)

    # Printing the rows of the grid
    for i in range(puzzle_size):
        row_labels = ""
        for char in range(puzzle_size):
            tile_label = list_of_tiles[i * puzzle_size + char]
            if tile_label == "":
                tile_label = "    "
            elif int(tile_label) < 10:
                tile_label = f"  {tile_label} "
            else:
                tile_label = f" {tile_label} "
            row_labels += f"│{tile_label}"
        row_labels += "│"
        print(row_labels)

        # Printing the separators of the grid
        if i != puzzle_size - 1:
            separator = "├" + "────┼" * (puzzle_size - 1) + "────┤"
            print(separator)

    # Printing the bottom border of the grid
    bottom_border = "└" + "────┴" * (puzzle_size - 1) + "────┘"
    print(bottom_border)


# Asks user for their choice input & determines if valid or not
def milestone_2(tiles):
    milestone_1(tiles)
    list_of_tiles = tiles.split(",")
    puzzle_size = int(len(list_of_tiles) ** 0.5)

    def is_vertically_adjacent(tiles_index):
        return abs(tiles_index // puzzle_size - blank_index // puzzle_size) <= 1 and \
               tiles_index % puzzle_size == blank_index % puzzle_size

    def is_horizontally_adjacent(tiles_index):
        return abs(tiles_index % puzzle_size - blank_index % puzzle_size) <= 1 and \
               tiles_index // puzzle_size == blank_index // puzzle_size

    while True:
        choice = input("Your move: ")
        if choice == "quit":
            print(f"{choice} is valid.")
            return
        elif choice.isdigit():
            tiles_index = list_of_tiles.index(choice)
            blank_index = list_of_tiles.index("")
            if is_vertically_adjacent(tiles_index) or is_horizontally_adjacent(tiles_index):
                print(f"{choice} is valid.")
                return
            else:
                print(f"{choice} is not valid. Try again.")
        else:
            print(f"{choice} is not valid. Try again.")
#input
#milestone_2("1,2,3,4,5,6,7,8,9,10,12,,13,14,11,15")


#milestone 3: final sliding puzzle
# Printing the grid board
def milestone_1(tiles):
    list_of_tiles = tiles.split(",")
    puzzle_size = int(len(list_of_tiles) ** 0.5)

    # Printing the top border of the grid
    top_border = (f"┌{'────┬' * (puzzle_size - 1)}────┐")
    print(top_border)

    # Printing the rows of the grid
    for i in range(puzzle_size):
        row_labels = ""
        for char in range(puzzle_size):
            tile_label = list_of_tiles[i * puzzle_size + char]
            if tile_label == "":
                tile_label = "    "
            elif int(tile_label) < 10:
                tile_label = (f"  {tile_label} ")
            else:
                tile_label = (f" {tile_label} ")
            row_labels += (f"│{tile_label}")
        row_labels += "│"
        print(row_labels)

        # Printing the separators of the grid
        if i != puzzle_size - 1:
            separator = (f"├{'────┼' * (puzzle_size - 1)}────┤")
            print(separator)

    # Printing the bottom border of the grid
    bottom_border = (f"└{'────┴' * (puzzle_size - 1)}────┘")
    print(bottom_border)


# Function to ask user for their move and determine if it's valid
def milestone_2(tiles):
    list_of_tiles = tiles.split(",")
    puzzle_size = int(len(list_of_tiles) ** 0.5)

    # Determine if a tile is vertically adjacent to the empty tile
    def is_vertically_adjacent(tiles_index):
        return abs(tiles_index // puzzle_size - blank_index // puzzle_size) <= 1 and \
               tiles_index % puzzle_size == blank_index % puzzle_size

    # Determine if a tile is horizontally adjacent to the empty tile
    def is_horizontally_adjacent(tiles_index):
        return abs(tiles_index % puzzle_size - blank_index % puzzle_size) <= 1 and \
               tiles_index // puzzle_size == blank_index // puzzle_size

    # Loop to get valid user input
    while True:
        choice = input("Your move: ")
        if choice == "quit":
            print(f"{choice} is valid.")
            return choice
        elif choice.isdigit():
            tiles_index = list_of_tiles.index(choice)
            blank_index = list_of_tiles.index("")
            if is_vertically_adjacent(tiles_index) or is_horizontally_adjacent(tiles_index):
                return choice
            else:
                print(f"{choice} is not valid. Try again.")
        else:
            print(f"{choice} is not valid. Try again.")

# Swap the chosen tile with the empty tile
def make_move(list_of_tiles, choice):
    tile_index, blank_index = list_of_tiles.index(choice), list_of_tiles.index("")
    list_of_tiles[tile_index], list_of_tiles[blank_index] = list_of_tiles[blank_index], list_of_tiles[tile_index]
    return list_of_tiles

# Check when the puzzle grid is complete
def is_puzzle_complete(list_of_tiles):
    correct_list = [int(a) if a else 0 for a in list_of_tiles]
    if 0 not in correct_list:
        return False
    else:
        blank_index = correct_list.index(0)
        if correct_list[:blank_index] == sorted(correct_list[:blank_index]) and blank_index == len(correct_list) - 1:
            return True
        else: return False

# Playing the puzzle grid
def main(tiles):
    moves = 0
    list_of_tiles = tiles.split(",")
    milestone_1(",".join(list_of_tiles))
    while not is_puzzle_complete(list_of_tiles):
        choice = milestone_2(",".join(list_of_tiles))
        if choice == "quit":
            return choice
        else:
            list_of_tiles = make_move(list_of_tiles, choice)
            moves += 1
            milestone_1(",".join(list_of_tiles))
    print(f"You won in {moves} moves. Congratulations!")
#input
main("1,2,3,4,5,6,7,8,9,10,12,,13,14,11,15")

