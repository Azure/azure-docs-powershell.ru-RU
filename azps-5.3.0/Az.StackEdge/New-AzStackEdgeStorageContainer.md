---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 5c0af3ed67bd7cba3408b6628de70c7064120954
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422764"
---
# <span data-ttu-id="376fd-101">New-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="376fd-101">New-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="376fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="376fd-102">SYNOPSIS</span></span>
<span data-ttu-id="376fd-103">Создает новый контейнер хранилища в учетной записи edge Storage на устройстве.</span><span class="sxs-lookup"><span data-stu-id="376fd-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="376fd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="376fd-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="376fd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="376fd-105">DESCRIPTION</span></span>
<span data-ttu-id="376fd-106">Для создания нового контейнера хранилища в учетной записи Edge на устройстве Stack Edge создается новый контейнер хранилища **New-AzStackEdgeStorageContainer.**</span><span class="sxs-lookup"><span data-stu-id="376fd-106">The **New-AzStackEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Stack Edge device.</span></span>

## <span data-ttu-id="376fd-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="376fd-107">EXAMPLES</span></span>

### <span data-ttu-id="376fd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="376fd-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="376fd-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="376fd-109">PARAMETERS</span></span>

### <span data-ttu-id="376fd-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="376fd-110">-AsJob</span></span>
<span data-ttu-id="376fd-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="376fd-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="376fd-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="376fd-112">-DataFormat</span></span>
<span data-ttu-id="376fd-113">Set Data Format ex: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="376fd-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="376fd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="376fd-114">-DefaultProfile</span></span>
<span data-ttu-id="376fd-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="376fd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="376fd-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="376fd-116">-DeviceName</span></span>
<span data-ttu-id="376fd-117">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="376fd-117">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="376fd-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="376fd-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="376fd-119">Укайм существующее имя EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="376fd-119">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="376fd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="376fd-120">-Name</span></span>
<span data-ttu-id="376fd-121">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="376fd-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="376fd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="376fd-122">-ResourceGroupName</span></span>
<span data-ttu-id="376fd-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="376fd-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="376fd-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="376fd-124">-Confirm</span></span>
<span data-ttu-id="376fd-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="376fd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="376fd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="376fd-126">-WhatIf</span></span>
<span data-ttu-id="376fd-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="376fd-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="376fd-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="376fd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="376fd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="376fd-129">CommonParameters</span></span>
<span data-ttu-id="376fd-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="376fd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="376fd-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="376fd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="376fd-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="376fd-132">INPUTS</span></span>

### <span data-ttu-id="376fd-133">System.String</span><span class="sxs-lookup"><span data-stu-id="376fd-133">System.String</span></span>

## <span data-ttu-id="376fd-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="376fd-134">OUTPUTS</span></span>

### <span data-ttu-id="376fd-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="376fd-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="376fd-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="376fd-136">NOTES</span></span>

## <span data-ttu-id="376fd-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="376fd-137">RELATED LINKS</span></span>
