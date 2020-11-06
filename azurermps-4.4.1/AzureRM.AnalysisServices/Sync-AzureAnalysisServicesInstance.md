---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: a75ae79722fed99ce96b0a082f4f56ace998354e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559983"
---
# <span data-ttu-id="17b9d-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="17b9d-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="17b9d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="17b9d-102">SYNOPSIS</span></span>
<span data-ttu-id="17b9d-103">Синхронизирует указанную базу данных на указанном экземпляре сервера служб Analysis Services со всеми экземплярами масштабирования запросов в среде, которая в настоящее время зарегистрирована, как указано в команде Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="17b9d-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17b9d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="17b9d-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="17b9d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17b9d-105">DESCRIPTION</span></span>
<span data-ttu-id="17b9d-106">Командлет Sync-AzureAnalysisServicesInstance синхронизирует указанную базу данных на указанном экземпляре сервера служб Analysis Services со всеми экземплярами масштабирования запросов в среде, которая в настоящее время зарегистрирована, как указано в Add-AzureAnalysisServicesAccount команде.</span><span class="sxs-lookup"><span data-stu-id="17b9d-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="17b9d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="17b9d-107">EXAMPLES</span></span>

### <span data-ttu-id="17b9d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="17b9d-108">Example 1</span></span>
```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="17b9d-109">Эта команда синхронизирует базу данных с именем SalesOrders на сервере с именем Contoso в среде westus.asazure.windows.net, в которой пользователь вошел в эту среду с помощью Add-AzureAnalysisServicesAccount команды.</span><span class="sxs-lookup"><span data-stu-id="17b9d-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="17b9d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="17b9d-110">PARAMETERS</span></span>

### <span data-ttu-id="17b9d-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="17b9d-111">-Instance</span></span>
<span data-ttu-id="17b9d-112">Имя экземпляра сервера служб Analysis Services, который нужно перезапустить</span><span class="sxs-lookup"><span data-stu-id="17b9d-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="17b9d-113">-База данных</span><span class="sxs-lookup"><span data-stu-id="17b9d-113">-Database</span></span>
<span data-ttu-id="17b9d-114">Идентификация базы данных, которую нужно синхронизировать</span><span class="sxs-lookup"><span data-stu-id="17b9d-114">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="17b9d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17b9d-115">-PassThru</span></span>
<span data-ttu-id="17b9d-116">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="17b9d-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="17b9d-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17b9d-117">-Confirm</span></span>
<span data-ttu-id="17b9d-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="17b9d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17b9d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17b9d-119">-WhatIf</span></span>
<span data-ttu-id="17b9d-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="17b9d-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17b9d-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="17b9d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17b9d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b9d-122">CommonParameters</span></span>
<span data-ttu-id="17b9d-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="17b9d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17b9d-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17b9d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b9d-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="17b9d-125">INPUTS</span></span>

## <span data-ttu-id="17b9d-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="17b9d-126">OUTPUTS</span></span>

### <span data-ttu-id="17b9d-127">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="17b9d-127">System.Boolean</span></span>

## <span data-ttu-id="17b9d-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="17b9d-128">NOTES</span></span>
<span data-ttu-id="17b9d-129">Alias (псевдоним): Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="17b9d-129">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="17b9d-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17b9d-130">RELATED LINKS</span></span>

