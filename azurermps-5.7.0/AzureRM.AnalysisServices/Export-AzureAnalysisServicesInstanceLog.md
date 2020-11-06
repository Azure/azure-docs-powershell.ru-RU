---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/export-azureanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: e93e38ef2914635cab61bf225c0d905d011ae643
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560399"
---
# <span data-ttu-id="b9349-101">Export-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="b9349-101">Export-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="b9349-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9349-102">SYNOPSIS</span></span>
<span data-ttu-id="b9349-103">Экспортирует журнал из экземпляра сервера служб Analysis Services в среде, которая в настоящее время зарегистрирована, как указано в команде Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b9349-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9349-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9349-104">SYNTAX</span></span>

```
Export-AzureAnalysisServicesInstanceLog [-Instance] <String> [-OutputPath] <String> [-WhatIf] [-Force]
```

## <span data-ttu-id="b9349-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9349-105">DESCRIPTION</span></span>
<span data-ttu-id="b9349-106">Командлет Export-AzureAnalysisServicesInstance экспортирует журнал из экземпляра сервера служб аналитики Azure в файл.</span><span class="sxs-lookup"><span data-stu-id="b9349-106">The Export-AzureAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="b9349-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9349-107">EXAMPLES</span></span>

### <span data-ttu-id="b9349-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b9349-108">Example 1</span></span>
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="b9349-109">Эта команда будет экспортировать журнал с сервера "TestServer" в среде, указанной в команде Add-AzureAnalysisServicesAccount, и сохранить ее в файле, указанном в элементе OutputPath "C:\path\to\log\testserver.log"</span><span class="sxs-lookup"><span data-stu-id="b9349-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="b9349-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9349-110">PARAMETERS</span></span>

### <span data-ttu-id="b9349-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="b9349-111">-Instance</span></span>
<span data-ttu-id="b9349-112">Имя экземпляра сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="b9349-112">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="b9349-113">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="b9349-113">-OutputPath</span></span>
<span data-ttu-id="b9349-114">Выходной путь к файлу для экспорта журнала</span><span class="sxs-lookup"><span data-stu-id="b9349-114">Output path to file to export log</span></span>

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

### <span data-ttu-id="b9349-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b9349-115">-Force</span></span>
<span data-ttu-id="b9349-116">Перезаписать файл, если он существует без запроса</span><span class="sxs-lookup"><span data-stu-id="b9349-116">Overwrite file if exists without asking</span></span>

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

## <span data-ttu-id="b9349-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9349-117">INPUTS</span></span>

### <span data-ttu-id="b9349-118">Ничего</span><span class="sxs-lookup"><span data-stu-id="b9349-118">None</span></span>
<span data-ttu-id="b9349-119">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b9349-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b9349-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9349-120">OUTPUTS</span></span>

## <span data-ttu-id="b9349-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9349-121">NOTES</span></span>
<span data-ttu-id="b9349-122">Alias (псевдоним): Export-AzureAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="b9349-122">Alias: Export-AzureAsInstanceLog</span></span>

## <span data-ttu-id="b9349-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9349-123">RELATED LINKS</span></span>

