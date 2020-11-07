---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: 5354737602f168245d6c4c8dca560698fa6cfac2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735071"
---
# <span data-ttu-id="02b3c-101">Export-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="02b3c-101">Export-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="02b3c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="02b3c-102">SYNOPSIS</span></span>
<span data-ttu-id="02b3c-103">Экспортирует журнал из экземпляра сервера служб Analysis Services в среде, которая в настоящее время зарегистрирована, как указано в команде Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="02b3c-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02b3c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="02b3c-104">SYNTAX</span></span>

```
Export-AzureAnalysisServicesInstanceLog [-Instance] <String> [-OutputPath] <String> [-WhatIf] [-Force]
```

## <span data-ttu-id="02b3c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02b3c-105">DESCRIPTION</span></span>
<span data-ttu-id="02b3c-106">Командлет Export-AzureAnalysisServicesInstance экспортирует журнал из экземпляра сервера служб аналитики Azure в файл.</span><span class="sxs-lookup"><span data-stu-id="02b3c-106">The Export-AzureAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="02b3c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="02b3c-107">EXAMPLES</span></span>

### <span data-ttu-id="02b3c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="02b3c-108">Example 1</span></span>
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="02b3c-109">Эта команда будет экспортировать журнал с сервера "TestServer" в среде, указанной в команде Add-AzureAnalysisServicesAccount, и сохранить ее в файле, указанном в элементе OutputPath "C:\path\to\log\testserver.log"</span><span class="sxs-lookup"><span data-stu-id="02b3c-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="02b3c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="02b3c-110">PARAMETERS</span></span>

### <span data-ttu-id="02b3c-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="02b3c-111">-Instance</span></span>
<span data-ttu-id="02b3c-112">Имя экземпляра сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="02b3c-112">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="02b3c-113">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="02b3c-113">-OutputPath</span></span>
<span data-ttu-id="02b3c-114">Выходной путь к файлу для экспорта журнала</span><span class="sxs-lookup"><span data-stu-id="02b3c-114">Output path to file to export log</span></span>

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

### <span data-ttu-id="02b3c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="02b3c-115">-Force</span></span>
<span data-ttu-id="02b3c-116">Перезаписать файл, если он существует без запроса</span><span class="sxs-lookup"><span data-stu-id="02b3c-116">Overwrite file if exists without asking</span></span>

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

## <span data-ttu-id="02b3c-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="02b3c-117">INPUTS</span></span>

## <span data-ttu-id="02b3c-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="02b3c-118">OUTPUTS</span></span>

## <span data-ttu-id="02b3c-119">Пуск</span><span class="sxs-lookup"><span data-stu-id="02b3c-119">NOTES</span></span>
<span data-ttu-id="02b3c-120">Alias (псевдоним): Export-AzureAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="02b3c-120">Alias: Export-AzureAsInstanceLog</span></span>

## <span data-ttu-id="02b3c-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02b3c-121">RELATED LINKS</span></span>

