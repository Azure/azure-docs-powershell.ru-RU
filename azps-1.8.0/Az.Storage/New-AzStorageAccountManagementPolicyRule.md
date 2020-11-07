---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
ms.openlocfilehash: 195ef931b942f3dc8a88ede7e3feb31a3b8aa77f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728626"
---
# <span data-ttu-id="0a44a-101">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="0a44a-101">New-AzStorageAccountManagementPolicyRule</span></span>

## <span data-ttu-id="0a44a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a44a-102">SYNOPSIS</span></span>
<span data-ttu-id="0a44a-103">Создает объект правила ManagementPolicy, который можно использовать в Set-AzStorageAccountManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="0a44a-103">Creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="0a44a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a44a-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyRule [-Name] <String> [-Disabled] -Action <PSManagementPolicyActionGroup>
 [-Filter <PSManagementPolicyRuleFilter>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a44a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a44a-105">DESCRIPTION</span></span>
<span data-ttu-id="0a44a-106">Командлет **New-AzStorageAccountManagementPolicyRule** создает объект правила ManagementPolicy, который можно использовать в Set-AzStorageAccountManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="0a44a-106">The **New-AzStorageAccountManagementPolicyRule** cmdlet creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="0a44a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a44a-107">EXAMPLES</span></span>

### <span data-ttu-id="0a44a-108">Пример 1: создание объекта правила ManagementPolicy, а затем Установка учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="0a44a-108">Example 1: Creates a ManagementPolicy rule object, then set to a Storage Account</span></span>
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

<span data-ttu-id="0a44a-109">Эта команда создает объект правила ManagementPolicy, при этом объект группы действий ManagementPolicy включает 4 действия, объект фильтра правила ManagementPolicy, а затем задает правило для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0a44a-109">This command create a ManagementPolicy rule object, with a ManagementPolicy action group object contains 4 actions, a ManagementPolicy rule filter object, then set the rule to a Storage Account.</span></span>

## <span data-ttu-id="0a44a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a44a-110">PARAMETERS</span></span>

### <span data-ttu-id="0a44a-111">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="0a44a-111">-Action</span></span>
<span data-ttu-id="0a44a-112">Объект, который определяет наборы макрокоманд.</span><span class="sxs-lookup"><span data-stu-id="0a44a-112">An object that defines the action set.</span></span>
<span data-ttu-id="0a44a-113">Получение объекта с помощью командлета Add-AzureStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="0a44a-113">Get the Object with cmdlet Add-AzureStorageAccountManagementPolicyAction</span></span>

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

### <span data-ttu-id="0a44a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a44a-114">-DefaultProfile</span></span>
<span data-ttu-id="0a44a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a44a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a44a-116">-Отключено</span><span class="sxs-lookup"><span data-stu-id="0a44a-116">-Disabled</span></span>
<span data-ttu-id="0a44a-117">Правило отключается, если оно задано.</span><span class="sxs-lookup"><span data-stu-id="0a44a-117">The rule is disabled if set it.</span></span>

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

### <span data-ttu-id="0a44a-118">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="0a44a-118">-Filter</span></span>
<span data-ttu-id="0a44a-119">Объект, который определяет наборы фильтров.</span><span class="sxs-lookup"><span data-stu-id="0a44a-119">An object that defines the filter set.</span></span>
<span data-ttu-id="0a44a-120">Получение объекта с помощью командлета New-AzureStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="0a44a-120">Get the Object with cmdlet New-AzureStorageAccountManagementPolicyFilter</span></span>

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

### <span data-ttu-id="0a44a-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0a44a-121">-Name</span></span>
<span data-ttu-id="0a44a-122">Имя правила может содержать любое сочетание букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="0a44a-122">A rule name can contain any combination of alpha numeric characters.</span></span>
<span data-ttu-id="0a44a-123">Имя правила задается с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="0a44a-123">Rule name is case-sensitive.</span></span>
<span data-ttu-id="0a44a-124">Оно должно быть уникальным в пределах политики.</span><span class="sxs-lookup"><span data-stu-id="0a44a-124">It must be unique within a policy.</span></span>

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

### <span data-ttu-id="0a44a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a44a-125">CommonParameters</span></span>
<span data-ttu-id="0a44a-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a44a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a44a-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a44a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a44a-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a44a-128">INPUTS</span></span>

### <span data-ttu-id="0a44a-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="0a44a-129">None</span></span>

## <span data-ttu-id="0a44a-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a44a-130">OUTPUTS</span></span>

### <span data-ttu-id="0a44a-131">Microsoft. Azure. Commands. Management. Storage. Models. PSManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="0a44a-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span></span>

## <span data-ttu-id="0a44a-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a44a-132">NOTES</span></span>

## <span data-ttu-id="0a44a-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a44a-133">RELATED LINKS</span></span>
