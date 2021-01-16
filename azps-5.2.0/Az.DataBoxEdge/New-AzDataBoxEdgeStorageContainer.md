---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 3561c77e79f0ee1be82b8f180fdf1b73879dc084
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407844"
---
# <span data-ttu-id="02ce8-101">New-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="02ce8-101">New-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="02ce8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02ce8-102">SYNOPSIS</span></span>
<span data-ttu-id="02ce8-103">Создает новый контейнер хранилища в учетной записи edge Storage на устройстве.</span><span class="sxs-lookup"><span data-stu-id="02ce8-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="02ce8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="02ce8-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02ce8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02ce8-105">DESCRIPTION</span></span>
<span data-ttu-id="02ce8-106">Для создания нового контейнера в учетной записи edge Storage на устройстве Edge создается новый контейнер хранилища **New-AzDataBoxEdgeStorageContainer.**</span><span class="sxs-lookup"><span data-stu-id="02ce8-106">The **New-AzDataBoxEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Data Box Edge device.</span></span>

## <span data-ttu-id="02ce8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="02ce8-107">EXAMPLES</span></span>

### <span data-ttu-id="02ce8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="02ce8-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="02ce8-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02ce8-109">PARAMETERS</span></span>

### <span data-ttu-id="02ce8-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02ce8-110">-AsJob</span></span>
<span data-ttu-id="02ce8-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="02ce8-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02ce8-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="02ce8-112">-DataFormat</span></span>
<span data-ttu-id="02ce8-113">Set Data Format ex: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="02ce8-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="02ce8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02ce8-114">-DefaultProfile</span></span>
<span data-ttu-id="02ce8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="02ce8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02ce8-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="02ce8-116">-DeviceName</span></span>
<span data-ttu-id="02ce8-117">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="02ce8-117">Device Name</span></span>

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

### <span data-ttu-id="02ce8-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="02ce8-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="02ce8-119">Укайм существующее имя EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="02ce8-119">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="02ce8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="02ce8-120">-Name</span></span>
<span data-ttu-id="02ce8-121">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="02ce8-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02ce8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02ce8-122">-ResourceGroupName</span></span>
<span data-ttu-id="02ce8-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="02ce8-123">Resource Group Name</span></span>

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

### <span data-ttu-id="02ce8-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02ce8-124">-Confirm</span></span>
<span data-ttu-id="02ce8-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02ce8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02ce8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02ce8-126">-WhatIf</span></span>
<span data-ttu-id="02ce8-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02ce8-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02ce8-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="02ce8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02ce8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02ce8-129">CommonParameters</span></span>
<span data-ttu-id="02ce8-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02ce8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02ce8-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02ce8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02ce8-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02ce8-132">INPUTS</span></span>

### <span data-ttu-id="02ce8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="02ce8-133">System.String</span></span>

## <span data-ttu-id="02ce8-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="02ce8-134">OUTPUTS</span></span>

### <span data-ttu-id="02ce8-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="02ce8-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="02ce8-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="02ce8-136">NOTES</span></span>

## <span data-ttu-id="02ce8-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02ce8-137">RELATED LINKS</span></span>