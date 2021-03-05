---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: 42e7b805e772e42ed395f8893b1140faaab715ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993919"
---
# <span data-ttu-id="086a5-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="086a5-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="086a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="086a5-102">SYNOPSIS</span></span>
<span data-ttu-id="086a5-103">Возвращает массив личных ид службы ссылок, который можно связать с закрытой конечной точкой с автоматическим утверждениями.</span><span class="sxs-lookup"><span data-stu-id="086a5-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="086a5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="086a5-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="086a5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="086a5-105">DESCRIPTION</span></span>
<span data-ttu-id="086a5-106">**Get-AzAutoApprovedPrivateLinkService** получает массив личных ид службы ссылок, который можно связать с частной конечной точкой с автоматическим утверждения.</span><span class="sxs-lookup"><span data-stu-id="086a5-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="086a5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="086a5-107">EXAMPLES</span></span>

### <span data-ttu-id="086a5-108">Пример</span><span class="sxs-lookup"><span data-stu-id="086a5-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="086a5-109">В этом примере возвращается массив личных ид службы ссылок, который можно связать с закрытой конечной точкой с автоматически утвержденным вариантом.</span><span class="sxs-lookup"><span data-stu-id="086a5-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="086a5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="086a5-110">PARAMETERS</span></span>

### <span data-ttu-id="086a5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="086a5-111">-DefaultProfile</span></span>
<span data-ttu-id="086a5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="086a5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="086a5-113">-Location</span><span class="sxs-lookup"><span data-stu-id="086a5-113">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="086a5-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="086a5-114">-ResourceGroupName</span></span>
<span data-ttu-id="086a5-115">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="086a5-115">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="086a5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="086a5-116">CommonParameters</span></span>
<span data-ttu-id="086a5-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="086a5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="086a5-118">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="086a5-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="086a5-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="086a5-119">INPUTS</span></span>

### <span data-ttu-id="086a5-120">Нет</span><span class="sxs-lookup"><span data-stu-id="086a5-120">None</span></span>

## <span data-ttu-id="086a5-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="086a5-121">OUTPUTS</span></span>

### <span data-ttu-id="086a5-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="086a5-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="086a5-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="086a5-123">NOTES</span></span>

## <span data-ttu-id="086a5-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="086a5-124">RELATED LINKS</span></span>
