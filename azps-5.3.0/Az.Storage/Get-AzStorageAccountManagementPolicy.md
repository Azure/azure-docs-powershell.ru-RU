---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/get-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: b27d6e8bec4dda2ba87a0b38a9b37a8d4739ae00
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504671"
---
# <span data-ttu-id="58260-101">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="58260-101">Get-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="58260-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58260-102">SYNOPSIS</span></span>
<span data-ttu-id="58260-103">Получает политику управления учетной записью хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="58260-103">Gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="58260-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="58260-104">SYNTAX</span></span>

### <span data-ttu-id="58260-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="58260-105">AccountName (Default)</span></span>
```
Get-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58260-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="58260-106">AccountResourceId</span></span>
```
Get-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58260-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="58260-107">AccountObject</span></span>
```
Get-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58260-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58260-108">DESCRIPTION</span></span>
<span data-ttu-id="58260-109">Для выполнения политики управления учетной записи хранилища Azure возвращается поле **Get-AzStorageAccountManagementPolicy.**</span><span class="sxs-lookup"><span data-stu-id="58260-109">The **Get-AzStorageAccountManagementPolicy** cmdlet gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="58260-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="58260-110">EXAMPLES</span></span>

### <span data-ttu-id="58260-111">Пример 1. Получите политику управления учетной записью хранения.</span><span class="sxs-lookup"><span data-stu-id="58260-111">Example 1: Get the management policy of a Storage account.</span></span>
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

<span data-ttu-id="58260-112">Эта команда получает политику управления учетной записью хранения.</span><span class="sxs-lookup"><span data-stu-id="58260-112">This command gets the management policy of a Storage account.</span></span>

## <span data-ttu-id="58260-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58260-113">PARAMETERS</span></span>

### <span data-ttu-id="58260-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58260-114">-DefaultProfile</span></span>
<span data-ttu-id="58260-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="58260-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58260-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58260-116">-ResourceGroupName</span></span>
<span data-ttu-id="58260-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="58260-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="58260-118">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="58260-118">-StorageAccount</span></span>
<span data-ttu-id="58260-119">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="58260-119">Storage account object</span></span>

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

### <span data-ttu-id="58260-120">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="58260-120">-StorageAccountName</span></span>
<span data-ttu-id="58260-121">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="58260-121">Storage Account Name.</span></span>

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

### <span data-ttu-id="58260-122">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="58260-122">-StorageAccountResourceId</span></span>
<span data-ttu-id="58260-123">ИД ресурса учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="58260-123">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="58260-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58260-124">CommonParameters</span></span>
<span data-ttu-id="58260-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58260-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58260-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58260-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58260-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58260-127">INPUTS</span></span>

### <span data-ttu-id="58260-128">System.String</span><span class="sxs-lookup"><span data-stu-id="58260-128">System.String</span></span>

## <span data-ttu-id="58260-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="58260-129">OUTPUTS</span></span>

### <span data-ttu-id="58260-130">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="58260-130">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="58260-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="58260-131">NOTES</span></span>

## <span data-ttu-id="58260-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58260-132">RELATED LINKS</span></span>
