---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 57fe2159ab53e1a822da376a07546202ac672cb2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516737"
---
# <span data-ttu-id="eeebd-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="eeebd-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="eeebd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eeebd-102">SYNOPSIS</span></span>
<span data-ttu-id="eeebd-103">Экспорт журнала с сервера Analysis Services в текущий логин в среде, как указано в Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="eeebd-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="eeebd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eeebd-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eeebd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eeebd-105">DESCRIPTION</span></span>
<span data-ttu-id="eeebd-106">Этот Export-AzAnalysisServicesInstance-файл экспортирует журнал из экземпляра сервера Служб Azure Analysis Services в файл.</span><span class="sxs-lookup"><span data-stu-id="eeebd-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="eeebd-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eeebd-107">EXAMPLES</span></span>

### <span data-ttu-id="eeebd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eeebd-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OutputPath C:\path\to\log\testserver.log
```

<span data-ttu-id="eeebd-109">Эта команда экспортирует журнал с сервера "testserver" в среде, указанной в команде Add-AzAnalysisServicesAccount, и сохраняет его в файл, указанный в OutputPath 'C:\path\to\log\testserver.log"</span><span class="sxs-lookup"><span data-stu-id="eeebd-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="eeebd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eeebd-110">PARAMETERS</span></span>

### <span data-ttu-id="eeebd-111">-Force</span><span class="sxs-lookup"><span data-stu-id="eeebd-111">-Force</span></span>
<span data-ttu-id="eeebd-112">Переписать файл, если он существует, без запроса</span><span class="sxs-lookup"><span data-stu-id="eeebd-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="eeebd-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="eeebd-113">-Instance</span></span>
<span data-ttu-id="eeebd-114">Имя экземпляра сервера Analysis Services</span><span class="sxs-lookup"><span data-stu-id="eeebd-114">Name of the Analysis Services server instance</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eeebd-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="eeebd-115">-OutputPath</span></span>
<span data-ttu-id="eeebd-116">Путь к выходным данным файла для экспорта журнала</span><span class="sxs-lookup"><span data-stu-id="eeebd-116">Output path to file to export log</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeebd-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eeebd-117">-PassThru</span></span>
<span data-ttu-id="eeebd-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="eeebd-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="eeebd-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eeebd-119">-Confirm</span></span>
<span data-ttu-id="eeebd-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="eeebd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeebd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeebd-121">-WhatIf</span></span>
<span data-ttu-id="eeebd-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeebd-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eeebd-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="eeebd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeebd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeebd-124">CommonParameters</span></span>
<span data-ttu-id="eeebd-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeebd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeebd-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeebd-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeebd-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eeebd-127">INPUTS</span></span>

### <span data-ttu-id="eeebd-128">Нет</span><span class="sxs-lookup"><span data-stu-id="eeebd-128">None</span></span>

## <span data-ttu-id="eeebd-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eeebd-129">OUTPUTS</span></span>

### <span data-ttu-id="eeebd-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="eeebd-130">System.Void</span></span>

## <span data-ttu-id="eeebd-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eeebd-131">NOTES</span></span>
<span data-ttu-id="eeebd-132">Псевдоним: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="eeebd-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="eeebd-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eeebd-133">RELATED LINKS</span></span>
