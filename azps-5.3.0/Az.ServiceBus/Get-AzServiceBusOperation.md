---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
ms.openlocfilehash: d1ae8cf3d0fd05acf4fa4897d362bd2cde70b346
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517469"
---
# <span data-ttu-id="e426d-101">Get-AzServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="e426d-101">Get-AzServiceBusOperation</span></span>

## <span data-ttu-id="e426d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e426d-102">SYNOPSIS</span></span>
<span data-ttu-id="e426d-103">Список поддерживаемых операций ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e426d-103">List supported ServiceBus Operations</span></span>

## <span data-ttu-id="e426d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e426d-104">SYNTAX</span></span>

```
Get-AzServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e426d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e426d-105">DESCRIPTION</span></span>
<span data-ttu-id="e426d-106">С **его нал., azServiceBusOperation выведется** список поддерживаемых операций ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="e426d-106">The **Get-AzServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="e426d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e426d-107">EXAMPLES</span></span>

### <span data-ttu-id="e426d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e426d-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusOperation
```

<span data-ttu-id="e426d-109">Списки поддерживаемых операций ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e426d-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="e426d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e426d-110">PARAMETERS</span></span>

### <span data-ttu-id="e426d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e426d-111">-DefaultProfile</span></span>
<span data-ttu-id="e426d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e426d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e426d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e426d-113">CommonParameters</span></span>
<span data-ttu-id="e426d-114">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e426d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e426d-115">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e426d-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e426d-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e426d-116">INPUTS</span></span>

### <span data-ttu-id="e426d-117">Нет</span><span class="sxs-lookup"><span data-stu-id="e426d-117">None</span></span>

## <span data-ttu-id="e426d-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e426d-118">OUTPUTS</span></span>

### <span data-ttu-id="e426d-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="e426d-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="e426d-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e426d-120">NOTES</span></span>

## <span data-ttu-id="e426d-121">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e426d-121">RELATED LINKS</span></span>
