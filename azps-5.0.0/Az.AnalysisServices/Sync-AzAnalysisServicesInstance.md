---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: 185b152d3fe4ac4cb7d80acb6d33c408911d626d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246473"
---
# <span data-ttu-id="b398b-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="b398b-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="b398b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b398b-102">SYNOPSIS</span></span>

<span data-ttu-id="b398b-103">Синхронизирует указанную базу данных на указанном экземпляре сервера служб Analysis Services со всеми экземплярами масштабирования запросов в среде, которая в настоящее время зарегистрирована, как указано в команде Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b398b-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="b398b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b398b-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b398b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b398b-105">DESCRIPTION</span></span>

<span data-ttu-id="b398b-106">Командлет Sync-AzAnalysisServicesInstance синхронизирует указанную базу данных на указанном экземпляре сервера служб Analysis Services со всеми экземплярами масштабирования запросов в среде, которая в настоящее время зарегистрирована, как указано в Add-AzAnalysisServicesAccount команде.</span><span class="sxs-lookup"><span data-stu-id="b398b-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="b398b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b398b-107">EXAMPLES</span></span>

### <span data-ttu-id="b398b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b398b-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="b398b-109">Эта команда синхронизирует базу данных с именем SalesOrders на сервере с именем Contoso в среде westus.asazure.windows.net, в которой пользователь вошел в эту среду с помощью Add-AzAnalysisServicesAccount команды.</span><span class="sxs-lookup"><span data-stu-id="b398b-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this environment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="b398b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b398b-110">PARAMETERS</span></span>

### <span data-ttu-id="b398b-111">-База данных</span><span class="sxs-lookup"><span data-stu-id="b398b-111">-Database</span></span>

<span data-ttu-id="b398b-112">Идентификация базы данных, которую нужно синхронизировать</span><span class="sxs-lookup"><span data-stu-id="b398b-112">Identity of the database to be synchronized</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b398b-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="b398b-113">-Instance</span></span>

<span data-ttu-id="b398b-114">Имя экземпляра сервера служб Analysis Services, который нужно перезапустить</span><span class="sxs-lookup"><span data-stu-id="b398b-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="b398b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b398b-115">-PassThru</span></span>

<span data-ttu-id="b398b-116">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b398b-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="b398b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b398b-117">-Confirm</span></span>
<span data-ttu-id="b398b-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b398b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b398b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b398b-119">-WhatIf</span></span>
<span data-ttu-id="b398b-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b398b-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b398b-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b398b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b398b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b398b-122">CommonParameters</span></span>
<span data-ttu-id="b398b-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b398b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b398b-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b398b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b398b-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b398b-125">INPUTS</span></span>

### <span data-ttu-id="b398b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b398b-126">System.String</span></span>

## <span data-ttu-id="b398b-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b398b-127">OUTPUTS</span></span>

### <span data-ttu-id="b398b-128">Microsoft. Azure. Commands. AnalysisServices. в плане. Models. ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="b398b-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="b398b-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="b398b-129">NOTES</span></span>

<span data-ttu-id="b398b-130">Alias (псевдоним): Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="b398b-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="b398b-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b398b-131">RELATED LINKS</span></span>
