---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/restart-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
ms.openlocfilehash: 04097dc54bd013e481064678e20bcf9ed559ab0c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246480"
---
# <span data-ttu-id="c1034-101">Restart-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="c1034-101">Restart-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="c1034-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c1034-102">SYNOPSIS</span></span>
<span data-ttu-id="c1034-103">Перезапускает экземпляр сервера служб Analysis Services в среде, в которой в настоящее время выполнен вход, указанный в команде Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c1034-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="c1034-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c1034-104">SYNTAX</span></span>

```
Restart-AzAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1034-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1034-105">DESCRIPTION</span></span>
<span data-ttu-id="c1034-106">Командлет Restart-AzAnalysisServicesInstance перезапускает экземпляр сервера служб аналитики Azure.</span><span class="sxs-lookup"><span data-stu-id="c1034-106">The Restart-AzAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="c1034-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c1034-107">EXAMPLES</span></span>

### <span data-ttu-id="c1034-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c1034-108">Example 1</span></span>
```
PS C:\>Restart-AzAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="c1034-109">Эта команда перезапустит сервер "TestServer" в среде, указанной в команде Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c1034-109">This command will restart the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="c1034-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c1034-110">PARAMETERS</span></span>

### <span data-ttu-id="c1034-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="c1034-111">-Instance</span></span>
<span data-ttu-id="c1034-112">Имя экземпляра сервера служб Analysis Services, который нужно перезапустить</span><span class="sxs-lookup"><span data-stu-id="c1034-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="c1034-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1034-113">-PassThru</span></span>
<span data-ttu-id="c1034-114">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c1034-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c1034-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1034-115">-Confirm</span></span>
<span data-ttu-id="c1034-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c1034-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1034-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1034-117">-WhatIf</span></span>
<span data-ttu-id="c1034-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c1034-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1034-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c1034-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1034-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1034-120">CommonParameters</span></span>
<span data-ttu-id="c1034-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c1034-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1034-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1034-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1034-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c1034-123">INPUTS</span></span>

### <span data-ttu-id="c1034-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="c1034-124">None</span></span>

## <span data-ttu-id="c1034-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1034-125">OUTPUTS</span></span>

### <span data-ttu-id="c1034-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c1034-126">System.Boolean</span></span>

## <span data-ttu-id="c1034-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="c1034-127">NOTES</span></span>
<span data-ttu-id="c1034-128">Alias (псевдоним): Restart-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="c1034-128">Alias: Restart-AzAsInstance</span></span>

## <span data-ttu-id="c1034-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1034-129">RELATED LINKS</span></span>