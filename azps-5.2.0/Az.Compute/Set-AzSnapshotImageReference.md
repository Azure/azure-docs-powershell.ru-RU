---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
ms.openlocfilehash: deb122735b94ed8ac0de63330a9fbdb3ecac81d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416711"
---
# <span data-ttu-id="fc388-101">Set-AzSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="fc388-101">Set-AzSnapshotImageReference</span></span>

## <span data-ttu-id="fc388-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc388-102">SYNOPSIS</span></span>
<span data-ttu-id="fc388-103">Задает свойства ссылки на изображение объекта моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="fc388-103">Sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="fc388-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fc388-104">SYNTAX</span></span>

```
Set-AzSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc388-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc388-105">DESCRIPTION</span></span>
<span data-ttu-id="fc388-106">Cmdlet **Set-AzSnapshotImageReference** задает свойства ссылки на изображение объекта моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="fc388-106">The **Set-AzSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="fc388-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fc388-107">EXAMPLES</span></span>

### <span data-ttu-id="fc388-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fc388-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="fc388-109">Первая команда создает локальный объект моментального снимка с размером 10 ГБ Premium_LRS типа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="fc388-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="fc388-110">Она также задает тип ОС Windows.</span><span class="sxs-lookup"><span data-stu-id="fc388-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="fc388-111">Вторая команда задает для объекта моментального снимка ИД изображения и логическую единицу 0.</span><span class="sxs-lookup"><span data-stu-id="fc388-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="fc388-112">Последняя команда принимает объект моментального снимка и создает моментальный снимок с именем "Моментальный снимок01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="fc388-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="fc388-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc388-113">PARAMETERS</span></span>

### <span data-ttu-id="fc388-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc388-114">-DefaultProfile</span></span>
<span data-ttu-id="fc388-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fc388-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc388-116">-Id</span><span class="sxs-lookup"><span data-stu-id="fc388-116">-Id</span></span>
<span data-ttu-id="fc388-117">Определяет ИД.</span><span class="sxs-lookup"><span data-stu-id="fc388-117">Specifies the ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc388-118">-Lun</span><span class="sxs-lookup"><span data-stu-id="fc388-118">-Lun</span></span>
<span data-ttu-id="fc388-119">Определяет логический номер единицы (LUN).</span><span class="sxs-lookup"><span data-stu-id="fc388-119">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc388-120">-Моментальный снимок</span><span class="sxs-lookup"><span data-stu-id="fc388-120">-Snapshot</span></span>
<span data-ttu-id="fc388-121">Определяет локальный объект моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="fc388-121">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc388-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc388-122">-Confirm</span></span>
<span data-ttu-id="fc388-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="fc388-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc388-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc388-124">-WhatIf</span></span>
<span data-ttu-id="fc388-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc388-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc388-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fc388-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc388-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc388-127">CommonParameters</span></span>
<span data-ttu-id="fc388-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc388-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc388-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc388-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc388-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc388-130">INPUTS</span></span>

### <span data-ttu-id="fc388-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="fc388-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="fc388-132">System.String</span><span class="sxs-lookup"><span data-stu-id="fc388-132">System.String</span></span>

### <span data-ttu-id="fc388-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="fc388-133">System.Int32</span></span>

## <span data-ttu-id="fc388-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fc388-134">OUTPUTS</span></span>

### <span data-ttu-id="fc388-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="fc388-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="fc388-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fc388-136">NOTES</span></span>

## <span data-ttu-id="fc388-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc388-137">RELATED LINKS</span></span>
