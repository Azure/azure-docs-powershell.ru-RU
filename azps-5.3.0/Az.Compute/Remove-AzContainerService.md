---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
ms.openlocfilehash: 8e029309099b3f28c1a9f0108bf4e6f4a78cb45d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519562"
---
# <span data-ttu-id="c1cee-101">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="c1cee-101">Remove-AzContainerService</span></span>

## <span data-ttu-id="c1cee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1cee-102">SYNOPSIS</span></span>
<span data-ttu-id="c1cee-103">Удаляет службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="c1cee-103">Removes a container service.</span></span>

## <span data-ttu-id="c1cee-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c1cee-104">SYNTAX</span></span>

```
Remove-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1cee-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1cee-105">DESCRIPTION</span></span>
<span data-ttu-id="c1cee-106">С **использованием cmdlet Remove-AzContainerService** служба контейнера удаляется из вашей учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="c1cee-106">The **Remove-AzContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="c1cee-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c1cee-107">EXAMPLES</span></span>

### <span data-ttu-id="c1cee-108">Пример 1. Удаление службы контейнера</span><span class="sxs-lookup"><span data-stu-id="c1cee-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="c1cee-109">Эта команда удаляет службу контейнеров cSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="c1cee-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="c1cee-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1cee-110">PARAMETERS</span></span>

### <span data-ttu-id="c1cee-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1cee-111">-AsJob</span></span>
<span data-ttu-id="c1cee-112">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="c1cee-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c1cee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1cee-113">-DefaultProfile</span></span>
<span data-ttu-id="c1cee-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c1cee-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1cee-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c1cee-115">-Force</span></span>
<span data-ttu-id="c1cee-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="c1cee-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c1cee-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c1cee-117">-Name</span></span>
<span data-ttu-id="c1cee-118">Указывает имя службы контейнеров, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1cee-118">Specifies the name of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c1cee-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1cee-119">-ResourceGroupName</span></span>
<span data-ttu-id="c1cee-120">Определяет группу ресурсов службы контейнеров, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1cee-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c1cee-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1cee-121">-Confirm</span></span>
<span data-ttu-id="c1cee-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1cee-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1cee-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1cee-123">-WhatIf</span></span>
<span data-ttu-id="c1cee-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1cee-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1cee-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c1cee-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1cee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1cee-126">CommonParameters</span></span>
<span data-ttu-id="c1cee-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1cee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1cee-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1cee-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1cee-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1cee-129">INPUTS</span></span>

### <span data-ttu-id="c1cee-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c1cee-130">System.String</span></span>

## <span data-ttu-id="c1cee-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c1cee-131">OUTPUTS</span></span>

### <span data-ttu-id="c1cee-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="c1cee-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="c1cee-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c1cee-133">NOTES</span></span>

## <span data-ttu-id="c1cee-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1cee-134">RELATED LINKS</span></span>

[<span data-ttu-id="c1cee-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="c1cee-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="c1cee-136">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="c1cee-136">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="c1cee-137">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="c1cee-137">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


