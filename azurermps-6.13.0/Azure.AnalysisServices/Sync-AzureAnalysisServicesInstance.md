---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 732eb92a46fa7e69ba5274398de648c16142ae75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558692"
---
# <span data-ttu-id="005a0-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="005a0-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="005a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="005a0-102">SYNOPSIS</span></span>

<span data-ttu-id="005a0-103">Синхронизирует указанную базу данных на указанном экземпляре сервера служб Analysis Services со всеми экземплярами масштабирования запросов в среде, которая в настоящее время зарегистрирована, как указано в команде Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="005a0-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="005a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="005a0-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="005a0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="005a0-105">DESCRIPTION</span></span>

<span data-ttu-id="005a0-106">Командлет Sync-AzureAnalysisServicesInstance синхронизирует указанную базу данных на указанном экземпляре сервера служб Analysis Services со всеми экземплярами масштабирования запросов в среде, которая в настоящее время зарегистрирована, как указано в Add-AzureAnalysisServicesAccount команде.</span><span class="sxs-lookup"><span data-stu-id="005a0-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="005a0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="005a0-107">EXAMPLES</span></span>

### <span data-ttu-id="005a0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="005a0-108">Example 1</span></span>

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="005a0-109">Эта команда синхронизирует базу данных с именем SalesOrders на сервере с именем Contoso в среде westus.asazure.windows.net, в которой пользователь вошел в эту среду с помощью Add-AzureAnalysisServicesAccount команды.</span><span class="sxs-lookup"><span data-stu-id="005a0-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="005a0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="005a0-110">PARAMETERS</span></span>

### <span data-ttu-id="005a0-111">-База данных</span><span class="sxs-lookup"><span data-stu-id="005a0-111">-Database</span></span>

<span data-ttu-id="005a0-112">Идентификация базы данных, которую нужно синхронизировать</span><span class="sxs-lookup"><span data-stu-id="005a0-112">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="005a0-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="005a0-113">-Instance</span></span>

<span data-ttu-id="005a0-114">Имя экземпляра сервера служб Analysis Services, который нужно перезапустить</span><span class="sxs-lookup"><span data-stu-id="005a0-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="005a0-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="005a0-115">-PassThru</span></span>

<span data-ttu-id="005a0-116">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="005a0-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="005a0-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="005a0-117">-Confirm</span></span>
<span data-ttu-id="005a0-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="005a0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="005a0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="005a0-119">-WhatIf</span></span>
<span data-ttu-id="005a0-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="005a0-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="005a0-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="005a0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="005a0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="005a0-122">CommonParameters</span></span>
<span data-ttu-id="005a0-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="005a0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="005a0-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="005a0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="005a0-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="005a0-125">INPUTS</span></span>

### <span data-ttu-id="005a0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="005a0-126">System.String</span></span>
<span data-ttu-id="005a0-127">Параметры: база данных (ByValue), экземпляр (ByValue)</span><span class="sxs-lookup"><span data-stu-id="005a0-127">Parameters: Database (ByValue), Instance (ByValue)</span></span>

## <span data-ttu-id="005a0-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="005a0-128">OUTPUTS</span></span>

### <span data-ttu-id="005a0-129">Microsoft. Azure. Commands. AnalysisServices. в плане. Models. ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="005a0-129">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="005a0-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="005a0-130">NOTES</span></span>

<span data-ttu-id="005a0-131">Alias (псевдоним): Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="005a0-131">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="005a0-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="005a0-132">RELATED LINKS</span></span>
