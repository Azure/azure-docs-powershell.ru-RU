---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: 15ecd8c0e22438016ea0f589cf798ecbcb65188f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519564"
---
# <span data-ttu-id="bcb2c-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="bcb2c-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="bcb2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcb2c-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb2c-103">Удаляет набор доступности из Azure.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="bcb2c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bcb2c-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcb2c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcb2c-105">DESCRIPTION</span></span>
<span data-ttu-id="bcb2c-106">С **использованием cmdlet Remove-AzAvailabilitySet** набор доступности удаляется из Azure.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="bcb2c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bcb2c-107">EXAMPLES</span></span>

### <span data-ttu-id="bcb2c-108">Пример 1. Удаление набора доступности</span><span class="sxs-lookup"><span data-stu-id="bcb2c-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="bcb2c-109">Эта команда удаляет набор доступности с именем AvailabilitySet03 в группе ресурсов "Группа ресурсов11".</span><span class="sxs-lookup"><span data-stu-id="bcb2c-109">This command removes an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="bcb2c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcb2c-110">PARAMETERS</span></span>

### <span data-ttu-id="bcb2c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bcb2c-111">-AsJob</span></span>
<span data-ttu-id="bcb2c-112">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="bcb2c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcb2c-113">-DefaultProfile</span></span>
<span data-ttu-id="bcb2c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcb2c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bcb2c-115">-Force</span></span>
<span data-ttu-id="bcb2c-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb2c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bcb2c-117">-Name</span></span>
<span data-ttu-id="bcb2c-118">Имя набора доступности.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-118">The availability set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcb2c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcb2c-119">-ResourceGroupName</span></span>
<span data-ttu-id="bcb2c-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="bcb2c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bcb2c-121">-Confirm</span></span>
<span data-ttu-id="bcb2c-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb2c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcb2c-123">-WhatIf</span></span>
<span data-ttu-id="bcb2c-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcb2c-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb2c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb2c-126">CommonParameters</span></span>
<span data-ttu-id="bcb2c-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb2c-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bcb2c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb2c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bcb2c-129">INPUTS</span></span>

### <span data-ttu-id="bcb2c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="bcb2c-130">System.String</span></span>

## <span data-ttu-id="bcb2c-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bcb2c-131">OUTPUTS</span></span>

### <span data-ttu-id="bcb2c-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bcb2c-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="bcb2c-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bcb2c-133">NOTES</span></span>

## <span data-ttu-id="bcb2c-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bcb2c-134">RELATED LINKS</span></span>

[<span data-ttu-id="bcb2c-135">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="bcb2c-135">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="bcb2c-136">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="bcb2c-136">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)


