---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/get-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: b27d6e8bec4dda2ba87a0b38a9b37a8d4739ae00
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066768"
---
# <span data-ttu-id="0ee5f-101">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0ee5f-101">Get-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="0ee5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0ee5f-102">SYNOPSIS</span></span>
<span data-ttu-id="0ee5f-103">Получает политику управления для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-103">Gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="0ee5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0ee5f-104">SYNTAX</span></span>

### <span data-ttu-id="0ee5f-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0ee5f-105">AccountName (Default)</span></span>
```
Get-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ee5f-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="0ee5f-106">AccountResourceId</span></span>
```
Get-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ee5f-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="0ee5f-107">AccountObject</span></span>
```
Get-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ee5f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ee5f-108">DESCRIPTION</span></span>
<span data-ttu-id="0ee5f-109">Командлет **Get-AzStorageAccountManagementPolicy** получает политику управления учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-109">The **Get-AzStorageAccountManagementPolicy** cmdlet gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="0ee5f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0ee5f-110">EXAMPLES</span></span>

### <span data-ttu-id="0ee5f-111">Пример 1: получение политики управления для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-111">Example 1: Get the management policy of a Storage account.</span></span>
```
PS C:\>Get-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 7:04:05 AM
Rules              : [
                         {
                             "Enabled":  true,
                             "Name":  "Test",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  {
                                                                                                    "DaysAfterModificationGreaterThan":  30
                                                                                                },
                                                                                 "TierToArchive":  {
                                                                                                       "DaysAfterModificationGreaterThan":  50
                                                                                                   },
                                                                                 "Delete":  {
                                                                                                "DaysAfterModificationGreaterThan":  100
                                                                                            }
                                                                             },
                                                                "Snapshot":  {
                                                                                 "Delete":  {
                                                                                                "DaysAfterCreationGreaterThan":  100
                                                                                            }
                                                                             }
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  [
                                                                                    "prefix1",
                                                                                    "prefix2"
                                                                                ],
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         },
                         {
                             "Enabled":  true,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  null,
                                                                                 "TierToArchive":  null,
                                                                                 "Delete":  {
                                                                                                "DaysAfterModificationGreaterThan":  100
                                                                                            }
                                                                             },
                                                                "Snapshot":  null
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="0ee5f-112">Эта команда получает политику управления учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-112">This command gets the management policy of a Storage account.</span></span>

## <span data-ttu-id="0ee5f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0ee5f-113">PARAMETERS</span></span>

### <span data-ttu-id="0ee5f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ee5f-114">-DefaultProfile</span></span>
<span data-ttu-id="0ee5f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ee5f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ee5f-116">-ResourceGroupName</span></span>
<span data-ttu-id="0ee5f-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-117">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ee5f-118">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="0ee5f-118">-StorageAccount</span></span>
<span data-ttu-id="0ee5f-119">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="0ee5f-119">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ee5f-120">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0ee5f-120">-StorageAccountName</span></span>
<span data-ttu-id="0ee5f-121">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-121">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ee5f-122">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="0ee5f-122">-StorageAccountResourceId</span></span>
<span data-ttu-id="0ee5f-123">Идентификатор ресурса учетной записи хранилища.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-123">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ee5f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ee5f-124">CommonParameters</span></span>
<span data-ttu-id="0ee5f-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0ee5f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ee5f-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ee5f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ee5f-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0ee5f-127">INPUTS</span></span>

### <span data-ttu-id="0ee5f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0ee5f-128">System.String</span></span>

## <span data-ttu-id="0ee5f-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ee5f-129">OUTPUTS</span></span>

### <span data-ttu-id="0ee5f-130">Microsoft. Azure. Management. Storage. Models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0ee5f-130">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="0ee5f-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="0ee5f-131">NOTES</span></span>

## <span data-ttu-id="0ee5f-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ee5f-132">RELATED LINKS</span></span>
