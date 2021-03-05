---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: 65bce04c3df14a6b9dc4397d47577d0642746c45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976184"
---
# <span data-ttu-id="cdad1-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="cdad1-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="cdad1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdad1-102">SYNOPSIS</span></span>
<span data-ttu-id="cdad1-103">Добавляет действие к объекту входной группы действий ManagementPolicy или создает объект Группы действий ManagementPolicy вместе с ней.</span><span class="sxs-lookup"><span data-stu-id="cdad1-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="cdad1-104">Объект можно использовать в new-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="cdad1-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="cdad1-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cdad1-105">SYNTAX</span></span>

### <span data-ttu-id="cdad1-106">BaseBlob (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cdad1-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdad1-107">Снимок</span><span class="sxs-lookup"><span data-stu-id="cdad1-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdad1-108">BlobVersion</span><span class="sxs-lookup"><span data-stu-id="cdad1-108">BlobVersion</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BlobVersionAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdad1-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cdad1-109">DESCRIPTION</span></span>
<span data-ttu-id="cdad1-110">Cmdlet **Add-AzStorageAccountManagementPolicyAction** добавляет действие к объекту входной группы действий ManagementPolicy или создает объект Группы действий ManagementPolicy с этим действием.</span><span class="sxs-lookup"><span data-stu-id="cdad1-110">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="cdad1-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cdad1-111">EXAMPLES</span></span>

### <span data-ttu-id="cdad1-112">Пример 1. Создание объекта группы действий ManagementPolicy с 4 действиями, его добавление в правило политики управления и настройка учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="cdad1-112">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action
PS C:\>$action 

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 30
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 50
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 100
Snapshot.TierToCool.DaysAfterCreationGreaterThan        : 
Snapshot.TierToArchive.DaysAfterCreationGreaterThan     : 
Snapshot.Delete.DaysAfterCreationGreaterThan            : 100
Version.TierToCool.DaysAfterCreationGreaterThan         : 
Version.TierToArchive.DaysAfterCreationGreaterThan      : 
Version.Delete.DaysAfterCreationGreaterThan             : 

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="cdad1-113">Первая команда создает объект группы действий ManagementPolicy, следующие 3 команды добавляют к этому объекту три действия.</span><span class="sxs-lookup"><span data-stu-id="cdad1-113">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="cdad1-114">Затем добавьте его в правило политики управления и установите учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="cdad1-114">Then add it to a management policy rule and set to a Storage account.</span></span>

### <span data-ttu-id="cdad1-115">Пример 2. Создание объекта группы действий ManagementPolicy с 6 действиями для моментального снимка и версии BLOB-объектов, его добавление в правило политики управления и настройка учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="cdad1-115">Example 2: Creates a ManagementPolicy Action Group object with 6 actions on snapshot and blob version, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction  -SnapshotAction Delete -daysAfterCreationGreaterThan 40
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -SnapshotAction TierToArchive -daysAfterCreationGreaterThan 50
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -SnapshotAction TierToCool -daysAfterCreationGreaterThan 60
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction Delete -daysAfterCreationGreaterThan 70
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction TierToArchive -daysAfterCreationGreaterThan 80
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction TierToCool -daysAfterCreationGreaterThan 90
PS C:\> $action

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 
Snapshot.TierToCool.DaysAfterCreationGreaterThan        : 60
Snapshot.TierToArchive.DaysAfterCreationGreaterThan     : 50
Snapshot.Delete.DaysAfterCreationGreaterThan            : 40
Version.TierToCool.DaysAfterCreationGreaterThan         : 90
Version.TierToArchive.DaysAfterCreationGreaterThan      : 80
Version.Delete.DaysAfterCreationGreaterThan             : 70

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="cdad1-116">Первая команда создает объект группы действий ManagementPolicy, следующие 5 команд добавляют к этому объекту 5 действий для моментального снимка и версии BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="cdad1-116">The first command create a ManagementPolicy Action Group object, the following 5 commands add 5 actions on snapshot and blob version to the object.</span></span> <span data-ttu-id="cdad1-117">Затем добавьте его в правило политики управления и установите учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="cdad1-117">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="cdad1-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdad1-118">PARAMETERS</span></span>

### <span data-ttu-id="cdad1-119">-BaseBlobAction</span><span class="sxs-lookup"><span data-stu-id="cdad1-119">-BaseBlobAction</span></span>
<span data-ttu-id="cdad1-120">Действие политики управления для baseblob.</span><span class="sxs-lookup"><span data-stu-id="cdad1-120">The management policy action for baseblob.</span></span>

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

### <span data-ttu-id="cdad1-121">-BlobVersionAction</span><span class="sxs-lookup"><span data-stu-id="cdad1-121">-BlobVersionAction</span></span>
<span data-ttu-id="cdad1-122">Действие политики управления для версии BLOB-проекта.</span><span class="sxs-lookup"><span data-stu-id="cdad1-122">The management policy action for blob version.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobVersion
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdad1-123">-DaysAfterCreationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="cdad1-123">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="cdad1-124">Integer value indicating the age in days after creation.</span><span class="sxs-lookup"><span data-stu-id="cdad1-124">Integer value indicating the age in days after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Snapshot, BlobVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdad1-125">-DaysAfterModificationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="cdad1-125">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="cdad1-126">Integer value indicating the age in days after last modification.</span><span class="sxs-lookup"><span data-stu-id="cdad1-126">Integer value indicating the age in days after last modification.</span></span>

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

### <span data-ttu-id="cdad1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdad1-127">-DefaultProfile</span></span>
<span data-ttu-id="cdad1-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cdad1-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdad1-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdad1-129">-InputObject</span></span>
<span data-ttu-id="cdad1-130">Если вы укалите объект Action ManagementPolicy, будет назначено действие объекту входной action.</span><span class="sxs-lookup"><span data-stu-id="cdad1-130">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="cdad1-131">Если входных данных нет, будет создаваться новый объект-действие.</span><span class="sxs-lookup"><span data-stu-id="cdad1-131">If not input, will create a new action object.</span></span>

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

### <span data-ttu-id="cdad1-132">-SnapshotAction</span><span class="sxs-lookup"><span data-stu-id="cdad1-132">-SnapshotAction</span></span>
<span data-ttu-id="cdad1-133">Действие политики управления для моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="cdad1-133">The management policy action for snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: Snapshot
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdad1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdad1-134">CommonParameters</span></span>
<span data-ttu-id="cdad1-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdad1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdad1-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdad1-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdad1-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cdad1-137">INPUTS</span></span>

### <span data-ttu-id="cdad1-138">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="cdad1-138">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="cdad1-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cdad1-139">OUTPUTS</span></span>

### <span data-ttu-id="cdad1-140">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="cdad1-140">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="cdad1-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cdad1-141">NOTES</span></span>

## <span data-ttu-id="cdad1-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cdad1-142">RELATED LINKS</span></span>
