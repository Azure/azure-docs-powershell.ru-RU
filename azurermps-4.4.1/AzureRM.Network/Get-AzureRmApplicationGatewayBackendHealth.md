---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
ms.openlocfilehash: d3f5114243828623ba6c55e9694cc4250ae12657
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559692"
---
# <span data-ttu-id="a562b-101">Get-AzureRmApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="a562b-101">Get-AzureRmApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="a562b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a562b-102">SYNOPSIS</span></span>
<span data-ttu-id="a562b-103">Возвращает состояние внутренней системы шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="a562b-103">Gets application gateway backend health.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a562b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a562b-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String>
 [-ExpandResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a562b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a562b-105">DESCRIPTION</span></span>
<span data-ttu-id="a562b-106">Командлет Get-AzureRmApplicationGatewayBackendHealth получает состояние внутренних данных для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="a562b-106">The Get-AzureRmApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="a562b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a562b-107">EXAMPLES</span></span>

### <span data-ttu-id="a562b-108">--------------------------Пример 1: получение работоспособности базы данных без развернутых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a562b-108">--------------------------  Example 1: Gets backend health without expanded resources.</span></span>  --------------------------
<span data-ttu-id="a562b-109">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="a562b-109">@{paragraph=PS C:\\\>}</span></span>



















```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="a562b-110">Эта команда возвращает состояние работоспособности серверного шлюза приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $BackendHealth.</span><span class="sxs-lookup"><span data-stu-id="a562b-110">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="a562b-111">--------------------------Пример 1: получение работоспособности серверной системы с развернутыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="a562b-111">--------------------------  Example 1: Gets backend health with expanded resources.</span></span>  --------------------------
<span data-ttu-id="a562b-112">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="a562b-112">@{paragraph=PS C:\\\>}</span></span>



















```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="a562b-113">Эта команда возвращает состояние работоспособности серверной системы (с развернутыми ресурсами) для шлюза приложений с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $BackendHealth.</span><span class="sxs-lookup"><span data-stu-id="a562b-113">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="a562b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a562b-114">PARAMETERS</span></span>

### <span data-ttu-id="a562b-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="a562b-115">-ExpandResource</span></span>
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

### <span data-ttu-id="a562b-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a562b-116">-Name</span></span>
<span data-ttu-id="a562b-117">Указывает имя шлюза приложения, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a562b-117">Specifies the name of the application gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a562b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a562b-118">-ResourceGroupName</span></span>
<span data-ttu-id="a562b-119">Указывает имя группы ресурсов, которая содержит шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="a562b-119">Specifies the name of the resource group that contains the application gateway.</span></span>

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

### <span data-ttu-id="a562b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a562b-120">-DefaultProfile</span></span>
<span data-ttu-id="a562b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a562b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a562b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a562b-122">CommonParameters</span></span>
<span data-ttu-id="a562b-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a562b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a562b-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a562b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a562b-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a562b-125">INPUTS</span></span>

### <span data-ttu-id="a562b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a562b-126">System.String</span></span>

## <span data-ttu-id="a562b-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a562b-127">OUTPUTS</span></span>

### <span data-ttu-id="a562b-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="a562b-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="a562b-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="a562b-129">NOTES</span></span>
<span data-ttu-id="a562b-130">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="a562b-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="a562b-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a562b-131">RELATED LINKS</span></span>

[<span data-ttu-id="a562b-132">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a562b-132">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

