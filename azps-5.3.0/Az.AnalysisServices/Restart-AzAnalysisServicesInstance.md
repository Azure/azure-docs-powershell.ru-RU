---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/restart-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
ms.openlocfilehash: 04097dc54bd013e481064678e20bcf9ed559ab0c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516722"
---
# <span data-ttu-id="208fe-101">Restart-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="208fe-101">Restart-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="208fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="208fe-102">SYNOPSIS</span></span>
<span data-ttu-id="208fe-103">Перезапуск экземпляра сервера Analysis Services в текущий вход в среду в Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="208fe-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="208fe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="208fe-104">SYNTAX</span></span>

```
Restart-AzAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="208fe-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="208fe-105">DESCRIPTION</span></span>
<span data-ttu-id="208fe-106">С Restart-AzAnalysisServicesInstance-сервера перезапускится экземпляр сервера Служб Azure Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="208fe-106">The Restart-AzAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="208fe-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="208fe-107">EXAMPLES</span></span>

### <span data-ttu-id="208fe-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="208fe-108">Example 1</span></span>
```
PS C:\>Restart-AzAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="208fe-109">Эта команда перезапустит сервер тестов в среде, указанной в Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="208fe-109">This command will restart the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="208fe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="208fe-110">PARAMETERS</span></span>

### <span data-ttu-id="208fe-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="208fe-111">-Instance</span></span>
<span data-ttu-id="208fe-112">Имя экземпляра сервера Analysis Services для перезапуска</span><span class="sxs-lookup"><span data-stu-id="208fe-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="208fe-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="208fe-113">-PassThru</span></span>
<span data-ttu-id="208fe-114">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="208fe-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="208fe-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="208fe-115">-Confirm</span></span>
<span data-ttu-id="208fe-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="208fe-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="208fe-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="208fe-117">-WhatIf</span></span>
<span data-ttu-id="208fe-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="208fe-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="208fe-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="208fe-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="208fe-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="208fe-120">CommonParameters</span></span>
<span data-ttu-id="208fe-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="208fe-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="208fe-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="208fe-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="208fe-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="208fe-123">INPUTS</span></span>

### <span data-ttu-id="208fe-124">Нет</span><span class="sxs-lookup"><span data-stu-id="208fe-124">None</span></span>

## <span data-ttu-id="208fe-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="208fe-125">OUTPUTS</span></span>

### <span data-ttu-id="208fe-126">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="208fe-126">System.Boolean</span></span>

## <span data-ttu-id="208fe-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="208fe-127">NOTES</span></span>
<span data-ttu-id="208fe-128">Псевдоним: Restart-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="208fe-128">Alias: Restart-AzAsInstance</span></span>

## <span data-ttu-id="208fe-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="208fe-129">RELATED LINKS</span></span>
