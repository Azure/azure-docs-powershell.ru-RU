---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
ms.openlocfilehash: c2a20d19676cff15ff26792a81bfc09242c5e4c2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404111"
---
# <span data-ttu-id="e6edd-101">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="e6edd-101">New-AzStorageAccountManagementPolicyRule</span></span>

## <span data-ttu-id="e6edd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6edd-102">SYNOPSIS</span></span>
<span data-ttu-id="e6edd-103">Создание объекта правила ManagementPolicy, который можно использовать в окне Set-AzStorageAccountManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="e6edd-103">Creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="e6edd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e6edd-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyRule [-Name] <String> [-Disabled] -Action <PSManagementPolicyActionGroup>
 [-Filter <PSManagementPolicyRuleFilter>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6edd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6edd-105">DESCRIPTION</span></span>
<span data-ttu-id="e6edd-106">Cmdlet **New-AzStorageAccountManagementPolicyRule** создает объект Правило ManagementPolicy, который можно использовать в set-AzStorageAccountManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="e6edd-106">The **New-AzStorageAccountManagementPolicyRule** cmdlet creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="e6edd-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e6edd-107">EXAMPLES</span></span>

### <span data-ttu-id="e6edd-108">Пример 1. Создание объекта правила ManagementPolicy и настройка учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="e6edd-108">Example 1: Creates a ManagementPolicy rule object, then set to a Storage Account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2

PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name rule1 -Action $action -Filter $filter
PS C:\>$rule

Enabled    : True
Name       : rule1
Definition : {
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
                                                     "blobprefix1",
                                                     "blobprefix2"
                                                 ],
                                 "BlobTypes":  [
                                                   "blockBlob"
                                               ]
                             }
             }

PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="e6edd-109">Эта команда создает объект правило ManagementPolicy с объектом группы действий ManagementPolicy, который содержит 4 действия, объект фильтра правил ManagementPolicy, а затем настроит правило на учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="e6edd-109">This command create a ManagementPolicy rule object, with a ManagementPolicy action group object contains 4 actions, a ManagementPolicy rule filter object, then set the rule to a Storage Account.</span></span>

## <span data-ttu-id="e6edd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6edd-110">PARAMETERS</span></span>

### <span data-ttu-id="e6edd-111">-Action</span><span class="sxs-lookup"><span data-stu-id="e6edd-111">-Action</span></span>
<span data-ttu-id="e6edd-112">Объект, который определяет набор действий.</span><span class="sxs-lookup"><span data-stu-id="e6edd-112">An object that defines the action set.</span></span>
<span data-ttu-id="e6edd-113">Получить объект с помощью Add-AzureStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="e6edd-113">Get the Object with cmdlet Add-AzureStorageAccountManagementPolicyAction</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6edd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6edd-114">-DefaultProfile</span></span>
<span data-ttu-id="e6edd-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6edd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6edd-116">-Disabled</span><span class="sxs-lookup"><span data-stu-id="e6edd-116">-Disabled</span></span>
<span data-ttu-id="e6edd-117">Если правило настроено, оно отключается.</span><span class="sxs-lookup"><span data-stu-id="e6edd-117">The rule is disabled if set it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6edd-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="e6edd-118">-Filter</span></span>
<span data-ttu-id="e6edd-119">Объект, который определяет набор фильтров.</span><span class="sxs-lookup"><span data-stu-id="e6edd-119">An object that defines the filter set.</span></span>
<span data-ttu-id="e6edd-120">Получить объект с помощью New-AzureStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="e6edd-120">Get the Object with cmdlet New-AzureStorageAccountManagementPolicyFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6edd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e6edd-121">-Name</span></span>
<span data-ttu-id="e6edd-122">Имя правила может содержать любое сочетание букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="e6edd-122">A rule name can contain any combination of alpha numeric characters.</span></span>
<span data-ttu-id="e6edd-123">Имя правила в правилах внося в них с чувствительными к делу.</span><span class="sxs-lookup"><span data-stu-id="e6edd-123">Rule name is case-sensitive.</span></span>
<span data-ttu-id="e6edd-124">Он должен быть уникальным в политике.</span><span class="sxs-lookup"><span data-stu-id="e6edd-124">It must be unique within a policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6edd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6edd-125">CommonParameters</span></span>
<span data-ttu-id="e6edd-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6edd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6edd-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6edd-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6edd-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6edd-128">INPUTS</span></span>

### <span data-ttu-id="e6edd-129">Нет</span><span class="sxs-lookup"><span data-stu-id="e6edd-129">None</span></span>

## <span data-ttu-id="e6edd-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e6edd-130">OUTPUTS</span></span>

### <span data-ttu-id="e6edd-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="e6edd-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span></span>

## <span data-ttu-id="e6edd-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e6edd-132">NOTES</span></span>

## <span data-ttu-id="e6edd-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6edd-133">RELATED LINKS</span></span>
