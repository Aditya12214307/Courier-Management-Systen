# Courier-Management-Systen
#A Courier Management System built in C, designed to manage courier services efficiently. It supports key functionalities like tracking shipments, managing deliveries, updating customer details, and generating invoices. This project demonstrates the use of data structures and file handling in C for real-world applications.
// #include <stdio.h>
// #include <string.h>
// #define MAX_SHIPMENTS 100

// struct shipment
// {
//     char sender_name[50];
//     char receiver_name[50];
//     char sender_address[100];
//     char receiver_address[100];
//     float weight;
//     float cost;
//     char status[20];
// };

// int main()
// {
//     struct shipment shipments[MAX_SHIPMENTS];
//     int num_shipments = 0;
//     char password[50] = "Aditya";
//     char input_password[50];

//     printf("Enter password: ");
//     scanf("%s", input_password);

//     if (strcmp(password, input_password) != 0)
//     {
//         printf("Incorrect password. Exiting program...\n");
//         return 0;
//     }

//     int choice;
//     do
//     {
//         printf("\nCourier Management System Menu\n");
//         printf("1. Add new shipment\n");
//         printf("2. View shipment status\n");
//         printf("3. Update shipment status\n");
//         printf("4. Cancel shipment\n");
//         printf("5. Exit program\n");
//         printf("Enter choice: ");
//         scanf("%d", &choice);

//         switch (choice)
//         {
//         case 1:
//             if (num_shipments >= MAX_SHIPMENTS)
//             {
//                 printf("Maximum number of shipments reached. Cannot add more shipments.\n");
//             }
//             else
//             {
//                 printf("Enter sender name: ");
//                 scanf("%s", shipments[num_shipments].sender_name);
//                 printf("Enter receiver name: ");
//                 scanf("%s", shipments[num_shipments].receiver_name);
//                 printf("Enter sender address: ");
//                 scanf("%s", shipments[num_shipments].sender_address);
//                 printf("Enter receiver address: ");
//                 scanf("%s", shipments[num_shipments].receiver_address);
//                 printf("Enter weight (in kg): ");
//                 scanf("%f", &shipments[num_shipments].weight);
//                 shipments[num_shipments].cost = shipments[num_shipments].weight * 50.0;
//                 strcpy(shipments[num_shipments].status, "In transit");
//                 num_shipments++;
//                 printf("Shipment added successfully.\n");
//             }
//             break;
//         case 2:
//             if (num_shipments == 0)
//             {
//                 printf("No shipments found.\n");
//             }
//             else
//             {
//                 int shipment_id;
//                 printf("Enter shipment ID: ");
//                 scanf("%d", &shipment_id);
//                 if (shipment_id < 1 || shipment_id > num_shipments)
//                 {
//                     printf("Invalid shipment ID.\n");
//                 }
//                 else
//                 {
//                     printf("Sender name: %s\n", shipments[shipment_id - 1].sender_name);
//                     printf("Receiver name: %s\n", shipments[shipment_id - 1].receiver_name);
//                     printf("Sender address: %s\n", shipments[shipment_id - 1].sender_address);
//                     printf("Receiver address: %s\n", shipments[shipment_id - 1].receiver_address);
//                     printf("Weight: %.2f kg\n", shipments[shipment_id - 1].weight);
//                     printf("Cost: %.2f\n", shipments[shipment_id - 1].cost);
//                     printf("Status: %s\n", shipments[shipment_id - 1].status);
//                 }
//             }
//             break;
//         case 3:
//             if (num_shipments == 0)
//             {
//                 printf("No shipments found.\n");
//             }
//             else
//             {
//                 int shipment_id;
//                 printf("Enter shipment ID: ");
//                 scanf("%d", &shipment_id);

//                 if (shipment_id < 1 || shipment_id > num_shipments)
//                 {
//                     printf("Invalid shipment ID.\n");
//                 }
//                 else
//                 {
//                     printf("Current status: %s\n", shipments[shipment_id - 1].status);
//                     printf("Enter new status: ");
//                     scanf("%s", shipments[shipment_id - 1].status);
//                     printf("Status updated successfully.\n");
//                 }
//             }
//             break;
//         case 4:
//             if (num_shipments == 0)
//             {
//                 printf("No shipments found.\n");
//             }
//             else
//             {
//                 int shipment_id;
//                 printf("Enter shipment ID: ");
//                 scanf("%d", &shipment_id);
//                 if (shipment_id < 1 || shipment_id > num_shipments)
//                 {
//                     printf("Invalid shipment ID.\n");
//                 }
//                 else
//                 {
//                     for (int i = shipment_id - 1; i < num_shipments - 1; i++)
//                     {
//                         shipments[i] = shipments[i + 1];
//                     }
//                     num_shipments--;
//                     printf("Shipment cancelled successfully.\n");
//                 }
//             }
//             break;
//         case 5:
//             printf("Exiting program...\n");
//             break;
//         default:
//             printf("Invalid choice. Please enter a valid choice.\n");
//             break;
//         }
//     } while (choice != 5);
//     return 0;
// }
