---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: b03aad1f76c5151746d50e69bc48ccf10e60842f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223884"
---
# <span data-ttu-id="41efd-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="41efd-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="41efd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41efd-102">SYNOPSIS</span></span>
<span data-ttu-id="41efd-103">Возвращает массив личных ид службы ссылок, который можно связать с закрытой конечной точкой с автоматическим утверждениями.</span><span class="sxs-lookup"><span data-stu-id="41efd-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="41efd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="41efd-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41efd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41efd-105">DESCRIPTION</span></span>
<span data-ttu-id="41efd-106">**Get-AzAutoApprovedPrivateLinkService** получает массив личных ид службы ссылок, который можно связать с частной конечной точкой с автоматическим утверждения.</span><span class="sxs-lookup"><span data-stu-id="41efd-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="41efd-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="41efd-107">EXAMPLES</span></span>

### <span data-ttu-id="41efd-108">Пример</span><span class="sxs-lookup"><span data-stu-id="41efd-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="41efd-109">В этом примере возвращается массив личных ид службы ссылок, который можно связать с закрытой конечной точкой с автоматически утвержденным вариантом.</span><span class="sxs-lookup"><span data-stu-id="41efd-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="41efd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41efd-110">PARAMETERS</span></span>

### <span data-ttu-id="41efd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41efd-111">-DefaultProfile</span></span>
<span data-ttu-id="41efd-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41efd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41efd-113">-Location</span><span class="sxs-lookup"><span data-stu-id="41efd-113">-Location</span></span>
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

### <span data-ttu-id="41efd-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41efd-114">-ResourceGroupName</span></span>
<span data-ttu-id="41efd-115">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="41efd-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="41efd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41efd-116">CommonParameters</span></span>
<span data-ttu-id="41efd-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41efd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41efd-118">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41efd-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41efd-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41efd-119">INPUTS</span></span>

### <span data-ttu-id="41efd-120">Нет</span><span class="sxs-lookup"><span data-stu-id="41efd-120">None</span></span>

## <span data-ttu-id="41efd-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="41efd-121">OUTPUTS</span></span>

### <span data-ttu-id="41efd-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="41efd-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="41efd-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="41efd-123">NOTES</span></span>

## <span data-ttu-id="41efd-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41efd-124">RELATED LINKS</span></span>
