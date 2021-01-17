---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/set-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: b52dc34ddffb2234962888407ed67c487f4195c4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403324"
---
# <span data-ttu-id="25d82-101">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="25d82-101">Set-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="25d82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25d82-102">SYNOPSIS</span></span>
<span data-ttu-id="25d82-103">Создает или изменяет политику управления учетной записью хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="25d82-103">Creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="25d82-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="25d82-104">SYNTAX</span></span>

### <span data-ttu-id="25d82-105">AccountNamePolicyRule (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="25d82-105">AccountNamePolicyRule (Default)</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Rule <PSManagementPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25d82-106">AccountNamePolicyObject</span><span class="sxs-lookup"><span data-stu-id="25d82-106">AccountNamePolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Policy <PSManagementPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25d82-107">AccountObjectPolicyRule</span><span class="sxs-lookup"><span data-stu-id="25d82-107">AccountObjectPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25d82-108">AccountObjectPolicyObject</span><span class="sxs-lookup"><span data-stu-id="25d82-108">AccountObjectPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25d82-109">AccountResourceIdPolicyRule</span><span class="sxs-lookup"><span data-stu-id="25d82-109">AccountResourceIdPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25d82-110">AccountResourceIdPolicyObject</span><span class="sxs-lookup"><span data-stu-id="25d82-110">AccountResourceIdPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25d82-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25d82-111">DESCRIPTION</span></span>
<span data-ttu-id="25d82-112">**Cmdlet Set-AzStorageAccountManagementPolicy** создает или изменяет политику управления учетной записью хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="25d82-112">The **Set-AzStorageAccountManagementPolicy** cmdlet creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="25d82-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="25d82-113">EXAMPLES</span></span>

### <span data-ttu-id="25d82-114">Пример 1. Создание или обновление политики управления учетной записью хранения с помощью объектов правила ManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="25d82-114">Example 1: Create or update the management policy of a Storage account with ManagementPolicy rule objects.</span></span>
```
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -SnapshotAction Delete -daysAfterCreationGreaterThan 100
PS C:\>$filter1 = New-AzStorageAccountManagementPolicyFilter -PrefixMatch ab,cd 
PS C:\>$rule1 = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action1 -Filter $filter1

PS C:\>$action2 = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$filter2 = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule2 = New-AzStorageAccountManagementPolicyRule -Name Test2 -Action $action2 -Filter $filter2

PS C:\>Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule1,$rule2


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 10:29:29 AM
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

<span data-ttu-id="25d82-115">Эта команда сначала создает два объекта правила ManagementPolicy, а затем создает или обновляет политику управления учетной записью хранения с объектами правила 2 ManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="25d82-115">This command first create 2 ManagementPolicy rule objects, then creates or updates the management policy of a Storage account with the 2 ManagementPolicy rule objects.</span></span>

### <span data-ttu-id="25d82-116">Пример 2. Создание или обновление политики управления учетной записью хранения с помощью политики форматирования Json.</span><span class="sxs-lookup"><span data-stu-id="25d82-116">Example 2: Create or update the management policy of a Storage account with a Json format policy.</span></span>
```
PS C:\>Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Policy (@{
    Rules=(@{
        Enabled=$true;
        Name="Test";
        Definition=(@{
            Actions=(@{
                BaseBlob=(@{
                    TierToCool=@{DaysAfterModificationGreaterThan=30};
                    TierToArchive=@{DaysAfterModificationGreaterThan=50};
                    Delete=@{DaysAfterModificationGreaterThan=100};
                });
                Snapshot=(@{
                    Delete=@{DaysAfterCreationGreaterThan=100};
                });
            });
            Filters=(@{
                BlobTypes=@("blockBlob");
                PrefixMatch=@("prefix1","prefix2");
            })
        })
    },
    @{
        Enabled=$false;
        Name="Test2";
        Definition=(@{
            Actions=(@{
                BaseBlob=(@{
                    TierToCool=@{DaysAfterModificationGreaterThan=80};
                });
            });
            Filters=(@{
                BlobTypes=@("blockBlob");
            })
        })
    })
})


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 10:24:55 AM
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
                             "Enabled":  false,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  {
                                                                                                    "DaysAfterModificationGreaterThan":  80
                                                                                                },
                                                                                 "TierToArchive":  null,
                                                                                 "Delete":  null
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

<span data-ttu-id="25d82-117">Эта команда создает или обновляет политику управления учетной записью хранения с помощью политики форматирования json.</span><span class="sxs-lookup"><span data-stu-id="25d82-117">This command creates or updates the management policy of a Storage account with a json format policy.</span></span>

### <span data-ttu-id="25d82-118">Пример 3. Получить политику управления из учетной записи хранения, а затем настроить ее на другую учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="25d82-118">Example 3: Get the management policy from a Storage account, then set it to another Storage account.</span></span>
```
PS C:\>$outputPolicy = Get-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" | Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup2" -AccountName "mystorageaccount2"
```

<span data-ttu-id="25d82-119">Эта команда сначала получает политику управления из учетной записи хранения, а затем перенастроит ее на другую учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="25d82-119">This command first gets the management policy from a Storage account, then set it to another Storage account.</span></span>

## <span data-ttu-id="25d82-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25d82-120">PARAMETERS</span></span>

### <span data-ttu-id="25d82-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25d82-121">-DefaultProfile</span></span>
<span data-ttu-id="25d82-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="25d82-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25d82-123">-Политика</span><span class="sxs-lookup"><span data-stu-id="25d82-123">-Policy</span></span>
<span data-ttu-id="25d82-124">Объект политики управления, который нужно настроить</span><span class="sxs-lookup"><span data-stu-id="25d82-124">Management Policy Object to Set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy
Parameter Sets: AccountNamePolicyObject, AccountObjectPolicyObject, AccountResourceIdPolicyObject
Aliases: ManagementPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25d82-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25d82-125">-ResourceGroupName</span></span>
<span data-ttu-id="25d82-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="25d82-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNamePolicyRule, AccountNamePolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25d82-127">-Правило</span><span class="sxs-lookup"><span data-stu-id="25d82-127">-Rule</span></span>
<span data-ttu-id="25d82-128">Правила политики управления.</span><span class="sxs-lookup"><span data-stu-id="25d82-128">The Management Policy rules.</span></span> <span data-ttu-id="25d82-129">Получить объект с помощью New-AzStorageAccountManagementPolicyRule управления.</span><span class="sxs-lookup"><span data-stu-id="25d82-129">Get the object with New-AzStorageAccountManagementPolicyRule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule[]
Parameter Sets: AccountNamePolicyRule, AccountObjectPolicyRule, AccountResourceIdPolicyRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25d82-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="25d82-130">-StorageAccount</span></span>
<span data-ttu-id="25d82-131">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="25d82-131">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObjectPolicyRule, AccountObjectPolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25d82-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="25d82-132">-StorageAccountName</span></span>
<span data-ttu-id="25d82-133">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="25d82-133">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNamePolicyRule, AccountNamePolicyObject
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25d82-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="25d82-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="25d82-135">ИД ресурса учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="25d82-135">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceIdPolicyRule, AccountResourceIdPolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d82-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25d82-136">-Confirm</span></span>
<span data-ttu-id="25d82-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25d82-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25d82-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25d82-138">-WhatIf</span></span>
<span data-ttu-id="25d82-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25d82-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25d82-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="25d82-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25d82-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d82-141">CommonParameters</span></span>
<span data-ttu-id="25d82-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25d82-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d82-143">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25d82-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d82-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25d82-144">INPUTS</span></span>

### <span data-ttu-id="25d82-145">System.String</span><span class="sxs-lookup"><span data-stu-id="25d82-145">System.String</span></span>

## <span data-ttu-id="25d82-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="25d82-146">OUTPUTS</span></span>

### <span data-ttu-id="25d82-147">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="25d82-147">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy</span></span>

## <span data-ttu-id="25d82-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="25d82-148">NOTES</span></span>

## <span data-ttu-id="25d82-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25d82-149">RELATED LINKS</span></span>
