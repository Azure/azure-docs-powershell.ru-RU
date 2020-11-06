---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/restart-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 0a89ee592e6f6f6d4d9e56df6d7e4df32b010524
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565040"
---
# <span data-ttu-id="120a3-101">Restart-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="120a3-101">Restart-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="120a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="120a3-102">SYNOPSIS</span></span>
<span data-ttu-id="120a3-103">Перезапускает экземпляр сервера служб Analysis Services в среде, в которой в настоящее время выполнен вход, указанный в команде Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="120a3-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="120a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="120a3-104">SYNTAX</span></span>

```
Restart-AzureAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="120a3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="120a3-105">DESCRIPTION</span></span>
<span data-ttu-id="120a3-106">Командлет Restart-AzureAnalysisServicesInstance перезапускает экземпляр сервера служб аналитики Azure.</span><span class="sxs-lookup"><span data-stu-id="120a3-106">The Restart-AzureAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="120a3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="120a3-107">EXAMPLES</span></span>

### <span data-ttu-id="120a3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="120a3-108">Example 1</span></span>
```
PS C:\>Restart-AzureAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="120a3-109">Эта команда перезапустит сервер "TestServer" в среде, указанной в команде Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="120a3-109">This command will restart the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="120a3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="120a3-110">PARAMETERS</span></span>

### <span data-ttu-id="120a3-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="120a3-111">-Instance</span></span>
<span data-ttu-id="120a3-112">Имя экземпляра сервера служб Analysis Services, который нужно перезапустить</span><span class="sxs-lookup"><span data-stu-id="120a3-112">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120a3-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="120a3-113">-PassThru</span></span>
<span data-ttu-id="120a3-114">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="120a3-114">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120a3-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="120a3-115">-Confirm</span></span>
<span data-ttu-id="120a3-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="120a3-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120a3-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="120a3-117">-WhatIf</span></span>
<span data-ttu-id="120a3-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="120a3-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="120a3-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="120a3-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="120a3-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="120a3-120">INPUTS</span></span>

### <span data-ttu-id="120a3-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="120a3-121">None</span></span>
<span data-ttu-id="120a3-122">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="120a3-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="120a3-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="120a3-123">OUTPUTS</span></span>

### <span data-ttu-id="120a3-124">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="120a3-124">System.Boolean</span></span>

## <span data-ttu-id="120a3-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="120a3-125">NOTES</span></span>
<span data-ttu-id="120a3-126">Alias (псевдоним): Restart-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="120a3-126">Alias: Restart-AzureAsInstance</span></span>

## <span data-ttu-id="120a3-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="120a3-127">RELATED LINKS</span></span>

