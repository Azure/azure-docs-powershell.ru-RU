---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
ms.openlocfilehash: d1ae8cf3d0fd05acf4fa4897d362bd2cde70b346
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242240"
---
# <span data-ttu-id="1eb30-101">Get-AzServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="1eb30-101">Get-AzServiceBusOperation</span></span>

## <span data-ttu-id="1eb30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1eb30-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb30-103">Список поддерживаемых операций ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1eb30-103">List supported ServiceBus Operations</span></span>

## <span data-ttu-id="1eb30-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1eb30-104">SYNTAX</span></span>

```
Get-AzServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1eb30-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1eb30-105">DESCRIPTION</span></span>
<span data-ttu-id="1eb30-106">С **его нал., azServiceBusOperation выведется** список поддерживаемых операций ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="1eb30-106">The **Get-AzServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="1eb30-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1eb30-107">EXAMPLES</span></span>

### <span data-ttu-id="1eb30-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1eb30-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusOperation
```

<span data-ttu-id="1eb30-109">Списки поддерживаемых операций ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1eb30-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="1eb30-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1eb30-110">PARAMETERS</span></span>

### <span data-ttu-id="1eb30-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eb30-111">-DefaultProfile</span></span>
<span data-ttu-id="1eb30-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1eb30-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1eb30-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb30-113">CommonParameters</span></span>
<span data-ttu-id="1eb30-114">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eb30-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb30-115">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1eb30-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb30-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1eb30-116">INPUTS</span></span>

### <span data-ttu-id="1eb30-117">Нет</span><span class="sxs-lookup"><span data-stu-id="1eb30-117">None</span></span>

## <span data-ttu-id="1eb30-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1eb30-118">OUTPUTS</span></span>

### <span data-ttu-id="1eb30-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="1eb30-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="1eb30-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1eb30-120">NOTES</span></span>

## <span data-ttu-id="1eb30-121">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1eb30-121">RELATED LINKS</span></span>
