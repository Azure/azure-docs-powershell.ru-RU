---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 57fe2159ab53e1a822da376a07546202ac672cb2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403236"
---
# <span data-ttu-id="72fb2-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="72fb2-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="72fb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72fb2-102">SYNOPSIS</span></span>
<span data-ttu-id="72fb2-103">Экспорт журнала с сервера Analysis Services в текущий логин в среде, как указано в Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="72fb2-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="72fb2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="72fb2-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72fb2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72fb2-105">DESCRIPTION</span></span>
<span data-ttu-id="72fb2-106">Этот Export-AzAnalysisServicesInstance-файл экспортирует журнал из экземпляра сервера Azure Analysis Services в файл</span><span class="sxs-lookup"><span data-stu-id="72fb2-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="72fb2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="72fb2-107">EXAMPLES</span></span>

### <span data-ttu-id="72fb2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="72fb2-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OutputPath C:\path\to\log\testserver.log
```

<span data-ttu-id="72fb2-109">Эта команда экспортирует журнал с сервера "testserver" в среде, указанной в команде Add-AzAnalysisServicesAccount, и сохраняет его в файл, указанный в OutputPath 'C:\path\to\log\testserver.log"</span><span class="sxs-lookup"><span data-stu-id="72fb2-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="72fb2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72fb2-110">PARAMETERS</span></span>

### <span data-ttu-id="72fb2-111">-Force</span><span class="sxs-lookup"><span data-stu-id="72fb2-111">-Force</span></span>
<span data-ttu-id="72fb2-112">Переписать файл, если он существует, без запроса</span><span class="sxs-lookup"><span data-stu-id="72fb2-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="72fb2-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="72fb2-113">-Instance</span></span>
<span data-ttu-id="72fb2-114">Имя экземпляра сервера Analysis Services</span><span class="sxs-lookup"><span data-stu-id="72fb2-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="72fb2-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="72fb2-115">-OutputPath</span></span>
<span data-ttu-id="72fb2-116">Путь к выходным данным файла для экспорта журнала</span><span class="sxs-lookup"><span data-stu-id="72fb2-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="72fb2-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72fb2-117">-PassThru</span></span>
<span data-ttu-id="72fb2-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="72fb2-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="72fb2-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72fb2-119">-Confirm</span></span>
<span data-ttu-id="72fb2-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72fb2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72fb2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72fb2-121">-WhatIf</span></span>
<span data-ttu-id="72fb2-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72fb2-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72fb2-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="72fb2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72fb2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72fb2-124">CommonParameters</span></span>
<span data-ttu-id="72fb2-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72fb2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72fb2-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72fb2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72fb2-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="72fb2-127">INPUTS</span></span>

### <span data-ttu-id="72fb2-128">Нет</span><span class="sxs-lookup"><span data-stu-id="72fb2-128">None</span></span>

## <span data-ttu-id="72fb2-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="72fb2-129">OUTPUTS</span></span>

### <span data-ttu-id="72fb2-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="72fb2-130">System.Void</span></span>

## <span data-ttu-id="72fb2-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="72fb2-131">NOTES</span></span>
<span data-ttu-id="72fb2-132">Псевдоним: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="72fb2-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="72fb2-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72fb2-133">RELATED LINKS</span></span>
