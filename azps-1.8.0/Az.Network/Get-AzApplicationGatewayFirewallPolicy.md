---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 652583ff4425c0403440856a32be3b8107d771ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730658"
---
# <span data-ttu-id="1ddff-101">Get-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1ddff-101">Get-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="1ddff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1ddff-102">SYNOPSIS</span></span>
<span data-ttu-id="1ddff-103">Возвращает политику брандмауэра для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1ddff-103">Gets an application gateway firewall policy.</span></span>

## <span data-ttu-id="1ddff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1ddff-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFirewallPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ddff-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ddff-105">DESCRIPTION</span></span>
<span data-ttu-id="1ddff-106">Командлет **Get-AzApplicationGatewayFirewallPolicy** получает политику брандмауэра для шлюза приложений...</span><span class="sxs-lookup"><span data-stu-id="1ddff-106">The **Get-AzApplicationGatewayFirewallPolicy** cmdlet gets an application gateway firewall policy..</span></span>

## <span data-ttu-id="1ddff-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1ddff-107">EXAMPLES</span></span>

### <span data-ttu-id="1ddff-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1ddff-108">Example 1</span></span>
```powershell
PS C:\> $AppGwFirewallPolicy = Get-AzApplicationGatewayFirewallPolicy -Name "FirewallPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1ddff-109">Эта команда получает политику брандмауэра шлюза приложений с именем FirewallPolicy1, которая принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $AppGwFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="1ddff-109">This command gets the application gateway firewall policy named FirewallPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="1ddff-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1ddff-110">PARAMETERS</span></span>

### <span data-ttu-id="1ddff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ddff-111">-DefaultProfile</span></span>
<span data-ttu-id="1ddff-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1ddff-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ddff-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1ddff-113">-Name</span></span>
<span data-ttu-id="1ddff-114">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="1ddff-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ddff-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ddff-115">-ResourceGroupName</span></span>
<span data-ttu-id="1ddff-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1ddff-116">The resource group name.</span></span>

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

### <span data-ttu-id="1ddff-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ddff-117">CommonParameters</span></span>
<span data-ttu-id="1ddff-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1ddff-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ddff-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ddff-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ddff-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1ddff-120">INPUTS</span></span>

### <span data-ttu-id="1ddff-121">System. String</span><span class="sxs-lookup"><span data-stu-id="1ddff-121">System.String</span></span>

## <span data-ttu-id="1ddff-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ddff-122">OUTPUTS</span></span>

### <span data-ttu-id="1ddff-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1ddff-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="1ddff-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="1ddff-124">NOTES</span></span>

## <span data-ttu-id="1ddff-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ddff-125">RELATED LINKS</span></span>
