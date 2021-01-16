---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: ed876765e3b5eb9d306847958772d9205758f5d6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98418876"
---
# <span data-ttu-id="3a11d-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="3a11d-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="3a11d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a11d-102">SYNOPSIS</span></span>
<span data-ttu-id="3a11d-103">Добавляет действие к объекту входной группы действий ManagementPolicy или создает объект "Группа действий ManagementPolicy".</span><span class="sxs-lookup"><span data-stu-id="3a11d-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="3a11d-104">Объект можно использовать в new-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="3a11d-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="3a11d-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3a11d-105">SYNTAX</span></span>

### <span data-ttu-id="3a11d-106">BaseBlob (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3a11d-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a11d-107">Снимок</span><span class="sxs-lookup"><span data-stu-id="3a11d-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a11d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a11d-108">DESCRIPTION</span></span>
<span data-ttu-id="3a11d-109">Cmdlet **Add-AzStorageAccountManagementPolicyAction** добавляет действие к объекту входной группы действий ManagementPolicy или создает объект Группы действий ManagementPolicy с этой действием.</span><span class="sxs-lookup"><span data-stu-id="3a11d-109">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="3a11d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3a11d-110">EXAMPLES</span></span>

### <span data-ttu-id="3a11d-111">Пример 1. Создание объекта группы действий ManagementPolicy с 4 действиями, его добавление в правило политики управления и настройка учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="3a11d-111">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
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

<span data-ttu-id="3a11d-112">Первая команда создает объект группы действий ManagementPolicy, следующие 3 команды добавляют к этому объекту три действия.</span><span class="sxs-lookup"><span data-stu-id="3a11d-112">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="3a11d-113">Затем добавьте его в правило политики управления и установите учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="3a11d-113">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="3a11d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a11d-114">PARAMETERS</span></span>

### <span data-ttu-id="3a11d-115">-BaseBlobAction</span><span class="sxs-lookup"><span data-stu-id="3a11d-115">-BaseBlobAction</span></span>
<span data-ttu-id="3a11d-116">Действие политики управления для baseblob.</span><span class="sxs-lookup"><span data-stu-id="3a11d-116">The management policy action for baseblob.</span></span>

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

### <span data-ttu-id="3a11d-117">-DaysAfterCreationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="3a11d-117">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="3a11d-118">Integer value indicating the age in days after creation.</span><span class="sxs-lookup"><span data-stu-id="3a11d-118">Integer value indicating the age in days after creation.</span></span>

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

### <span data-ttu-id="3a11d-119">-DaysAfterModificationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="3a11d-119">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="3a11d-120">Integer value indicating the age in days after last modification.</span><span class="sxs-lookup"><span data-stu-id="3a11d-120">Integer value indicating the age in days after last modification.</span></span>

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

### <span data-ttu-id="3a11d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a11d-121">-DefaultProfile</span></span>
<span data-ttu-id="3a11d-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3a11d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a11d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a11d-123">-InputObject</span></span>
<span data-ttu-id="3a11d-124">Если вы ввести данные для объекта action ManagementPolicy, будет назначено действие объекту входной action.</span><span class="sxs-lookup"><span data-stu-id="3a11d-124">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="3a11d-125">Если входных данных нет, создается новый объект действия.</span><span class="sxs-lookup"><span data-stu-id="3a11d-125">If not input, will create a new action object.</span></span>

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

### <span data-ttu-id="3a11d-126">-SnapshotAction</span><span class="sxs-lookup"><span data-stu-id="3a11d-126">-SnapshotAction</span></span>
<span data-ttu-id="3a11d-127">Действие политики управления для моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="3a11d-127">The management policy action for snapshot.</span></span>

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

### <span data-ttu-id="3a11d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a11d-128">CommonParameters</span></span>
<span data-ttu-id="3a11d-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a11d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a11d-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a11d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a11d-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a11d-131">INPUTS</span></span>

### <span data-ttu-id="3a11d-132">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="3a11d-132">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="3a11d-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3a11d-133">OUTPUTS</span></span>

### <span data-ttu-id="3a11d-134">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="3a11d-134">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="3a11d-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3a11d-135">NOTES</span></span>

## <span data-ttu-id="3a11d-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a11d-136">RELATED LINKS</span></span>
