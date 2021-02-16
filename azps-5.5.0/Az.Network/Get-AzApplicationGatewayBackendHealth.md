---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
ms.openlocfilehash: 378c6ee91c438bfa70ab8e89e069ad81d3515e33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223932"
---
# <span data-ttu-id="ec88f-101">Get-AzApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="ec88f-101">Get-AzApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="ec88f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec88f-102">SYNOPSIS</span></span>
<span data-ttu-id="ec88f-103">Возвращает состояние backend шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="ec88f-103">Gets application gateway backend health.</span></span>

## <span data-ttu-id="ec88f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ec88f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String> [-ExpandResource <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec88f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec88f-105">DESCRIPTION</span></span>
<span data-ttu-id="ec88f-106">Для Get-AzApplicationGatewayBackendHealth шлюза приложений возвращается состояние безопасности шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="ec88f-106">The Get-AzApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="ec88f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ec88f-107">EXAMPLES</span></span>

### <span data-ttu-id="ec88f-108">Пример 1. Возвращается состояние backend без расширенных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ec88f-108">Example 1: Gets backend health without expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="ec88f-109">Эта команда получает состояние шлюза приложения ApplicationGateway01, которое принадлежит группе ресурсов ResourceGroup01, и сохраняет ее в переменной $BackendHealth ресурса.</span><span class="sxs-lookup"><span data-stu-id="ec88f-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="ec88f-110">Пример 2. Возвращает дополнительные возможности с расширенными ресурсами.</span><span class="sxs-lookup"><span data-stu-id="ec88f-110">Example 2: Gets backend health with expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="ec88f-111">Эта команда получает состояние системы (с расширенными ресурсами) шлюза приложения ApplicationGateway01, который принадлежит группе ресурсов ResourceGroup01, и сохраняет ее в переменной $BackendHealth.</span><span class="sxs-lookup"><span data-stu-id="ec88f-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="ec88f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec88f-112">PARAMETERS</span></span>

### <span data-ttu-id="ec88f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec88f-113">-AsJob</span></span>
<span data-ttu-id="ec88f-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ec88f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec88f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec88f-115">-DefaultProfile</span></span>
<span data-ttu-id="ec88f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ec88f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec88f-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="ec88f-117">-ExpandResource</span></span>
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

### <span data-ttu-id="ec88f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ec88f-118">-Name</span></span>
<span data-ttu-id="ec88f-119">Указывает имя шлюза приложения, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec88f-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec88f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec88f-120">-ResourceGroupName</span></span>
<span data-ttu-id="ec88f-121">Имя группы ресурсов, которая содержит шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="ec88f-121">Specifies the name of the resource group that contains the application gateway.</span></span>

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

### <span data-ttu-id="ec88f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec88f-122">CommonParameters</span></span>
<span data-ttu-id="ec88f-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec88f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec88f-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec88f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec88f-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec88f-125">INPUTS</span></span>

### <span data-ttu-id="ec88f-126">System.String</span><span class="sxs-lookup"><span data-stu-id="ec88f-126">System.String</span></span>

## <span data-ttu-id="ec88f-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ec88f-127">OUTPUTS</span></span>

### <span data-ttu-id="ec88f-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="ec88f-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="ec88f-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ec88f-129">NOTES</span></span>
<span data-ttu-id="ec88f-130">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="ec88f-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ec88f-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec88f-131">RELATED LINKS</span></span>

[<span data-ttu-id="ec88f-132">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ec88f-132">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

