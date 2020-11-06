---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 038c7456f849777f16ca0113d799b4ee8a16cd2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558051"
---
# <span data-ttu-id="c4179-101">Restart-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="c4179-101">Restart-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="c4179-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c4179-102">SYNOPSIS</span></span>
<span data-ttu-id="c4179-103">Перезапускает экземпляр сервера служб Analysis Services в среде, в которой в настоящее время выполнен вход, указанный в команде Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c4179-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4179-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c4179-104">SYNTAX</span></span>

```
Restart-AzureAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4179-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4179-105">DESCRIPTION</span></span>
<span data-ttu-id="c4179-106">Командлет Restart-AzureAnalysisServicesInstance перезапускает экземпляр сервера служб аналитики Azure.</span><span class="sxs-lookup"><span data-stu-id="c4179-106">The Restart-AzureAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="c4179-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c4179-107">EXAMPLES</span></span>

### <span data-ttu-id="c4179-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c4179-108">Example 1</span></span>
```
PS C:\>Restart-AzureAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="c4179-109">Эта команда перезапустит сервер "TestServer" в среде, указанной в команде Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c4179-109">This command will restart the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="c4179-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c4179-110">PARAMETERS</span></span>

### <span data-ttu-id="c4179-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="c4179-111">-Instance</span></span>
<span data-ttu-id="c4179-112">Имя экземпляра сервера служб Analysis Services, который нужно перезапустить</span><span class="sxs-lookup"><span data-stu-id="c4179-112">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4179-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4179-113">-PassThru</span></span>
<span data-ttu-id="c4179-114">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c4179-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c4179-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4179-115">-Confirm</span></span>
<span data-ttu-id="c4179-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c4179-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4179-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4179-117">-WhatIf</span></span>
<span data-ttu-id="c4179-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c4179-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4179-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c4179-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4179-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4179-120">CommonParameters</span></span>
<span data-ttu-id="c4179-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c4179-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4179-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4179-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4179-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c4179-123">INPUTS</span></span>

## <span data-ttu-id="c4179-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4179-124">OUTPUTS</span></span>

### <span data-ttu-id="c4179-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c4179-125">System.Boolean</span></span>

## <span data-ttu-id="c4179-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="c4179-126">NOTES</span></span>
<span data-ttu-id="c4179-127">Alias (псевдоним): Restart-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="c4179-127">Alias: Restart-AzureAsInstance</span></span>

## <span data-ttu-id="c4179-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4179-128">RELATED LINKS</span></span>

