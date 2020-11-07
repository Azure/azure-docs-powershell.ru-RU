---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: 73384827b5af2b3370eca1eee5a90066a89b8e55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906953"
---
# <span data-ttu-id="b575c-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="b575c-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="b575c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b575c-102">SYNOPSIS</span></span>
<span data-ttu-id="b575c-103">Добавляет действие в объект ManagementPolicy действия группы действий или создает объект группы действий ManagementPolicy с действием.</span><span class="sxs-lookup"><span data-stu-id="b575c-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="b575c-104">Объект можно использовать в New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="b575c-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="b575c-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b575c-105">SYNTAX</span></span>

### <span data-ttu-id="b575c-106">BaseBlob (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b575c-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b575c-107">Состояния</span><span class="sxs-lookup"><span data-stu-id="b575c-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b575c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b575c-108">DESCRIPTION</span></span>
<span data-ttu-id="b575c-109">Командлет **Add-AzStorageAccountManagementPolicyAction** добавляет действие в объект группы действий ввода ManagementPolicy или создает объект группы действий ManagementPolicy с действием.</span><span class="sxs-lookup"><span data-stu-id="b575c-109">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="b575c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b575c-110">EXAMPLES</span></span>

### <span data-ttu-id="b575c-111">Пример 1: создает объект группы действий ManagementPolicy с 4 действиями, затем добавляет его в правило политики управления и задается учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b575c-111">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action
PS C:\>$action 

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 30
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 50
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 100
Snapshot.Delete.DaysAfterCreationGreaterThan            : 100

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="b575c-112">В первой команде создается объект группы действий ManagementPolicy, поэтому следующие 3 команды добавляют в объект 3 действия.</span><span class="sxs-lookup"><span data-stu-id="b575c-112">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="b575c-113">Затем добавьте его в правило политики управления и установите для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b575c-113">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="b575c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b575c-114">PARAMETERS</span></span>

### <span data-ttu-id="b575c-115">-BaseBlobAction</span><span class="sxs-lookup"><span data-stu-id="b575c-115">-BaseBlobAction</span></span>
<span data-ttu-id="b575c-116">Действие политики управления для baseblob.</span><span class="sxs-lookup"><span data-stu-id="b575c-116">The management policy action for baseblob.</span></span>

```yaml
Type: System.String
Parameter Sets: BaseBlob
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b575c-117">-DaysAfterCreationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="b575c-117">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="b575c-118">Целочисленное значение, обозначающее возраст в днях после создания.</span><span class="sxs-lookup"><span data-stu-id="b575c-118">Integer value indicating the age in days after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Snapshot
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b575c-119">-DaysAfterModificationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="b575c-119">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="b575c-120">Целочисленное значение, обозначающее возраст в днях после последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="b575c-120">Integer value indicating the age in days after last modification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: BaseBlob
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b575c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b575c-121">-DefaultProfile</span></span>
<span data-ttu-id="b575c-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b575c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b575c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b575c-123">-InputObject</span></span>
<span data-ttu-id="b575c-124">Если вы настроили объект действия ManagementPolicy, он задаст нужное действие объекту входного действия.</span><span class="sxs-lookup"><span data-stu-id="b575c-124">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="b575c-125">Если значение не введено, создаст новый объект Action.</span><span class="sxs-lookup"><span data-stu-id="b575c-125">If not input, will create a new action object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b575c-126">-SnapshotAction</span><span class="sxs-lookup"><span data-stu-id="b575c-126">-SnapshotAction</span></span>
<span data-ttu-id="b575c-127">Действие политики управления для моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="b575c-127">The management policy action for snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: Snapshot
Aliases:
Accepted values: Delete

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b575c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b575c-128">CommonParameters</span></span>
<span data-ttu-id="b575c-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b575c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b575c-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b575c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b575c-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b575c-131">INPUTS</span></span>

### <span data-ttu-id="b575c-132">Microsoft. Azure. Commands. Management. Storage. Models. PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="b575c-132">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="b575c-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b575c-133">OUTPUTS</span></span>

### <span data-ttu-id="b575c-134">Microsoft. Azure. Commands. Management. Storage. Models. PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="b575c-134">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="b575c-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="b575c-135">NOTES</span></span>

## <span data-ttu-id="b575c-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b575c-136">RELATED LINKS</span></span>
