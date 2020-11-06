---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: f3fb2377fd78db4b330afd39a8691f958597f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560391"
---
# <span data-ttu-id="c17c7-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="c17c7-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="c17c7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c17c7-102">SYNOPSIS</span></span>

<span data-ttu-id="c17c7-103">Синхронизирует указанную базу данных на указанном экземпляре сервера служб Analysis Services со всеми экземплярами масштабирования запросов в среде, которая в настоящее время зарегистрирована, как указано в команде Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c17c7-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c17c7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c17c7-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-Passthru]
```

## <span data-ttu-id="c17c7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c17c7-105">DESCRIPTION</span></span>

<span data-ttu-id="c17c7-106">Командлет Sync-AzureAnalysisServicesInstance синхронизирует указанную базу данных на указанном экземпляре сервера служб Analysis Services со всеми экземплярами масштабирования запросов в среде, которая в настоящее время зарегистрирована, как указано в Add-AzureAnalysisServicesAccount команде.</span><span class="sxs-lookup"><span data-stu-id="c17c7-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="c17c7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c17c7-107">EXAMPLES</span></span>

### <span data-ttu-id="c17c7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c17c7-108">Example 1</span></span>

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="c17c7-109">Эта команда синхронизирует базу данных с именем SalesOrders на сервере с именем Contoso в среде westus.asazure.windows.net, в которой пользователь вошел в эту среду с помощью Add-AzureAnalysisServicesAccount команды.</span><span class="sxs-lookup"><span data-stu-id="c17c7-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="c17c7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c17c7-110">PARAMETERS</span></span>

### <span data-ttu-id="c17c7-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="c17c7-111">-Instance</span></span>

<span data-ttu-id="c17c7-112">Имя экземпляра сервера служб Analysis Services, который нужно перезапустить</span><span class="sxs-lookup"><span data-stu-id="c17c7-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="c17c7-113">-База данных</span><span class="sxs-lookup"><span data-stu-id="c17c7-113">-Database</span></span>

<span data-ttu-id="c17c7-114">Идентификация базы данных, которую нужно синхронизировать</span><span class="sxs-lookup"><span data-stu-id="c17c7-114">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="c17c7-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c17c7-115">-PassThru</span></span>

<span data-ttu-id="c17c7-116">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c17c7-116">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: Switch
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="c17c7-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c17c7-117">INPUTS</span></span>

### <span data-ttu-id="c17c7-118">Ничего</span><span class="sxs-lookup"><span data-stu-id="c17c7-118">None</span></span>
<span data-ttu-id="c17c7-119">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c17c7-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c17c7-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c17c7-120">OUTPUTS</span></span>

### <span data-ttu-id="c17c7-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c17c7-121">System.Boolean</span></span>

## <span data-ttu-id="c17c7-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="c17c7-122">NOTES</span></span>

<span data-ttu-id="c17c7-123">Alias (псевдоним): Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="c17c7-123">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="c17c7-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c17c7-124">RELATED LINKS</span></span>
