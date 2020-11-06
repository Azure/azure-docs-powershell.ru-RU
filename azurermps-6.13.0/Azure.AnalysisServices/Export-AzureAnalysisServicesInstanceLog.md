---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/export-azureanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: dad0e14b72c256706456ed3c923b966323fd7dad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561287"
---
# <span data-ttu-id="703d5-101">Export-AzureAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="703d5-101">Export-AzureAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="703d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="703d5-102">SYNOPSIS</span></span>
<span data-ttu-id="703d5-103">Экспортирует журнал из экземпляра сервера служб Analysis Services в среде, которая в настоящее время зарегистрирована, как указано в команде Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="703d5-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="703d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="703d5-104">SYNTAX</span></span>

```
Export-AzureAnalysisServicesInstanceLog -Instance <String> -OutputPath <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="703d5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="703d5-105">DESCRIPTION</span></span>
<span data-ttu-id="703d5-106">Командлет Export-AzureAnalysisServicesInstance экспортирует журнал из экземпляра сервера служб аналитики Azure в файл.</span><span class="sxs-lookup"><span data-stu-id="703d5-106">The Export-AzureAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="703d5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="703d5-107">EXAMPLES</span></span>

### <span data-ttu-id="703d5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="703d5-108">Example 1</span></span>
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="703d5-109">Эта команда будет экспортировать журнал с сервера "TestServer" в среде, указанной в команде Add-AzureAnalysisServicesAccount, и сохранить ее в файле, указанном в элементе OutputPath "C:\path\to\log\testserver.log"</span><span class="sxs-lookup"><span data-stu-id="703d5-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="703d5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="703d5-110">PARAMETERS</span></span>

### <span data-ttu-id="703d5-111">-Force</span><span class="sxs-lookup"><span data-stu-id="703d5-111">-Force</span></span>
<span data-ttu-id="703d5-112">Перезаписать файл, если он существует без запроса</span><span class="sxs-lookup"><span data-stu-id="703d5-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="703d5-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="703d5-113">-Instance</span></span>
<span data-ttu-id="703d5-114">Имя экземпляра сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="703d5-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="703d5-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="703d5-115">-OutputPath</span></span>
<span data-ttu-id="703d5-116">Выходной путь к файлу для экспорта журнала</span><span class="sxs-lookup"><span data-stu-id="703d5-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="703d5-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="703d5-117">-Confirm</span></span>
<span data-ttu-id="703d5-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="703d5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="703d5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="703d5-119">-WhatIf</span></span>
<span data-ttu-id="703d5-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="703d5-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="703d5-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="703d5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="703d5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="703d5-122">CommonParameters</span></span>
<span data-ttu-id="703d5-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="703d5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="703d5-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="703d5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="703d5-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="703d5-125">INPUTS</span></span>

### <span data-ttu-id="703d5-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="703d5-126">None</span></span>

## <span data-ttu-id="703d5-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="703d5-127">OUTPUTS</span></span>

### <span data-ttu-id="703d5-128">System. void</span><span class="sxs-lookup"><span data-stu-id="703d5-128">System.Void</span></span>

## <span data-ttu-id="703d5-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="703d5-129">NOTES</span></span>
<span data-ttu-id="703d5-130">Alias (псевдоним): Export-AzureAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="703d5-130">Alias: Export-AzureAsInstanceLog</span></span>

## <span data-ttu-id="703d5-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="703d5-131">RELATED LINKS</span></span>
