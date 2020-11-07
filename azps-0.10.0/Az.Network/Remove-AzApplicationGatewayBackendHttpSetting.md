---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-AzApplicationGatewayBackendHttpSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 168223e9e442b7aa37da11f3a1e0a092c3cb3efc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909565"
---
# <span data-ttu-id="d1404-101">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="d1404-101">Remove-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="d1404-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d1404-102">SYNOPSIS</span></span>
<span data-ttu-id="d1404-103">Удаляет из шлюза приложений параметры HTTP с внутренним интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="d1404-103">Removes back-end HTTP settings from an application gateway.</span></span>

## <span data-ttu-id="d1404-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d1404-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendHttpSetting -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1404-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1404-105">DESCRIPTION</span></span>
<span data-ttu-id="d1404-106">Командлет Remove-AzApplicationGatewayBackendHttpSetting удаляет параметры HTTP-протокола обратной передачи с шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="d1404-106">The Remove-AzApplicationGatewayBackendHttpSetting cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="d1404-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d1404-107">EXAMPLES</span></span>

### <span data-ttu-id="d1404-108">Пример 1: Удаление HTTP-параметров для серверных интерфейсов из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="d1404-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="d1404-109">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d1404-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="d1404-110">Вторая команда удаляет серверный параметр HTTP с именем BackEndSetting02 из шлюза приложения, который хранится в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d1404-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="d1404-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d1404-111">PARAMETERS</span></span>

### <span data-ttu-id="d1404-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1404-112">-ApplicationGateway</span></span>
<span data-ttu-id="d1404-113">Указывает шлюз приложений, с помощью которого этот командлет удаляет параметры HTTP для серверного элемента.</span><span class="sxs-lookup"><span data-stu-id="d1404-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1404-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1404-114">-DefaultProfile</span></span>
<span data-ttu-id="d1404-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d1404-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1404-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d1404-116">-Name</span></span>
<span data-ttu-id="d1404-117">Указывает имя серверных параметров HTTP, которые удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d1404-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1404-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1404-118">CommonParameters</span></span>
<span data-ttu-id="d1404-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d1404-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1404-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1404-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1404-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d1404-121">INPUTS</span></span>

### <span data-ttu-id="d1404-122">System. String</span><span class="sxs-lookup"><span data-stu-id="d1404-122">System.String</span></span>

## <span data-ttu-id="d1404-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1404-123">OUTPUTS</span></span>

### <span data-ttu-id="d1404-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1404-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d1404-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="d1404-125">NOTES</span></span>

## <span data-ttu-id="d1404-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1404-126">RELATED LINKS</span></span>

[<span data-ttu-id="d1404-127">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="d1404-127">Add-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="d1404-128">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="d1404-128">New-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="d1404-129">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="d1404-129">Get-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="d1404-130">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="d1404-130">Set-AzApplicationGatewayBackendHttpSetting</span></span>]()

