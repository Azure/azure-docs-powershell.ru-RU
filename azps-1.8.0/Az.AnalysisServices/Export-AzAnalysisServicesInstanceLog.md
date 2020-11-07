---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 04a1c63ac2ae1b0db692f2bef4b4803a8acb744f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720209"
---
# <span data-ttu-id="fa1e4-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="fa1e4-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="fa1e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fa1e4-102">SYNOPSIS</span></span>
<span data-ttu-id="fa1e4-103">Экспортирует журнал из экземпляра сервера служб Analysis Services в среде, которая в настоящее время зарегистрирована, как указано в команде Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fa1e4-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="fa1e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fa1e4-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa1e4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa1e4-105">DESCRIPTION</span></span>
<span data-ttu-id="fa1e4-106">Командлет Export-AzAnalysisServicesInstance экспортирует журнал из экземпляра сервера служб аналитики Azure в файл.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="fa1e4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fa1e4-107">EXAMPLES</span></span>

### <span data-ttu-id="fa1e4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fa1e4-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="fa1e4-109">Эта команда будет экспортировать журнал с сервера "TestServer" в среде, указанной в команде Add-AzAnalysisServicesAccount, и сохранить ее в файле, указанном в элементе OutputPath "C:\path\to\log\testserver.log"</span><span class="sxs-lookup"><span data-stu-id="fa1e4-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="fa1e4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fa1e4-110">PARAMETERS</span></span>

### <span data-ttu-id="fa1e4-111">-Force</span><span class="sxs-lookup"><span data-stu-id="fa1e4-111">-Force</span></span>
<span data-ttu-id="fa1e4-112">Перезаписать файл, если он существует без запроса</span><span class="sxs-lookup"><span data-stu-id="fa1e4-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="fa1e4-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="fa1e4-113">-Instance</span></span>
<span data-ttu-id="fa1e4-114">Имя экземпляра сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="fa1e4-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="fa1e4-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="fa1e4-115">-OutputPath</span></span>
<span data-ttu-id="fa1e4-116">Выходной путь к файлу для экспорта журнала</span><span class="sxs-lookup"><span data-stu-id="fa1e4-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="fa1e4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa1e4-117">-PassThru</span></span>
<span data-ttu-id="fa1e4-118">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="fa1e4-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fa1e4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa1e4-119">-Confirm</span></span>
<span data-ttu-id="fa1e4-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa1e4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa1e4-121">-WhatIf</span></span>
<span data-ttu-id="fa1e4-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa1e4-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa1e4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa1e4-124">CommonParameters</span></span>
<span data-ttu-id="fa1e4-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fa1e4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa1e4-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa1e4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa1e4-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fa1e4-127">INPUTS</span></span>

### <span data-ttu-id="fa1e4-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="fa1e4-128">None</span></span>

## <span data-ttu-id="fa1e4-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa1e4-129">OUTPUTS</span></span>

### <span data-ttu-id="fa1e4-130">System. void</span><span class="sxs-lookup"><span data-stu-id="fa1e4-130">System.Void</span></span>

## <span data-ttu-id="fa1e4-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="fa1e4-131">NOTES</span></span>
<span data-ttu-id="fa1e4-132">Alias (псевдоним): Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="fa1e4-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="fa1e4-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa1e4-133">RELATED LINKS</span></span>
