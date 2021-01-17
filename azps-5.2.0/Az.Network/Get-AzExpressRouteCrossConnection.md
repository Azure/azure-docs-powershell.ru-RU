---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: a6a3b973a893e3588b5df77700318a725bde11b9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391972"
---
# <span data-ttu-id="dfccd-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="dfccd-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="dfccd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfccd-102">SYNOPSIS</span></span>
<span data-ttu-id="dfccd-103">Получает перекрестное подключение Azure ExpressRoute из Azure.</span><span class="sxs-lookup"><span data-stu-id="dfccd-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="dfccd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dfccd-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfccd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfccd-105">DESCRIPTION</span></span>
<span data-ttu-id="dfccd-106">Для извлечения объекта перекрестного подключения ExpressRoute из подписки используется cmdlet **Get-AzExpressRouteCrossConnection.**</span><span class="sxs-lookup"><span data-stu-id="dfccd-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="dfccd-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="dfccd-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="dfccd-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dfccd-108">EXAMPLES</span></span>

### <span data-ttu-id="dfccd-109">Пример 1. Подключение ExpressRoute к интернету</span><span class="sxs-lookup"><span data-stu-id="dfccd-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="dfccd-110">Пример 2. Список перекрестных подключений ExpressRoute с помощью фильтра</span><span class="sxs-lookup"><span data-stu-id="dfccd-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="dfccd-111">Этот cmdlet will list all ExpressRoute cross connections that begin with "test"</span><span class="sxs-lookup"><span data-stu-id="dfccd-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="dfccd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfccd-112">PARAMETERS</span></span>

### <span data-ttu-id="dfccd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfccd-113">-DefaultProfile</span></span>
<span data-ttu-id="dfccd-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dfccd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfccd-115">-Name</span><span class="sxs-lookup"><span data-stu-id="dfccd-115">-Name</span></span>
<span data-ttu-id="dfccd-116">Имя перекрестного подключения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="dfccd-116">The name of the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="dfccd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfccd-117">-ResourceGroupName</span></span>
<span data-ttu-id="dfccd-118">Имя группы ресурсов, которая содержит перекрестное подключение ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="dfccd-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="dfccd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfccd-119">CommonParameters</span></span>
<span data-ttu-id="dfccd-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfccd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfccd-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dfccd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfccd-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dfccd-122">INPUTS</span></span>

### <span data-ttu-id="dfccd-123">Нет</span><span class="sxs-lookup"><span data-stu-id="dfccd-123">None</span></span>
<span data-ttu-id="dfccd-124">Этот cmdlet не принимает входные данные.</span><span class="sxs-lookup"><span data-stu-id="dfccd-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dfccd-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dfccd-125">OUTPUTS</span></span>

### <span data-ttu-id="dfccd-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="dfccd-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="dfccd-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dfccd-127">NOTES</span></span>

## <span data-ttu-id="dfccd-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dfccd-128">RELATED LINKS</span></span>

[<span data-ttu-id="dfccd-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="dfccd-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)