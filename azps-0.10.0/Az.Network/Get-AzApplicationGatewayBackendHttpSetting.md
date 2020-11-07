---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-AzApplicationGatewayBackendHttpSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 96872aa399c3241710e12e3b96a14e8678f21d83
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910102"
---
# <span data-ttu-id="a44d0-101">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a44d0-101">Get-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="a44d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a44d0-102">SYNOPSIS</span></span>
<span data-ttu-id="a44d0-103">Получает серверные параметры HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="a44d0-103">Gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="a44d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a44d0-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHttpSetting [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a44d0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a44d0-105">DESCRIPTION</span></span>
<span data-ttu-id="a44d0-106">Командлет Get-AzApplicationGatewayBackendHttpSetting получает серверные параметры HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="a44d0-106">The Get-AzApplicationGatewayBackendHttpSetting cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="a44d0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a44d0-107">EXAMPLES</span></span>

### <span data-ttu-id="a44d0-108">Пример 1: получение HTTP-параметров "на сервер" по имени</span><span class="sxs-lookup"><span data-stu-id="a44d0-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="a44d0-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет ее в переменной $AppGw. Вторая команда получает параметры HTTP с именем Settings01 для $AppGw и сохраняет параметры в переменной $Settings.</span><span class="sxs-lookup"><span data-stu-id="a44d0-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="a44d0-110">Пример 2: получение коллекции параметров HTTP для веб-части</span><span class="sxs-lookup"><span data-stu-id="a44d0-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw
```

<span data-ttu-id="a44d0-111">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет ее в переменной $AppGw. Вторая команда получает коллекцию параметров HTTP для $AppGw и сохраняет параметры в переменной $SettingsList.</span><span class="sxs-lookup"><span data-stu-id="a44d0-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="a44d0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a44d0-112">PARAMETERS</span></span>

### <span data-ttu-id="a44d0-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a44d0-113">-ApplicationGateway</span></span>
<span data-ttu-id="a44d0-114">Указывает объект шлюза приложения, который содержит параметры HTTP для внутренней стороны.</span><span class="sxs-lookup"><span data-stu-id="a44d0-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="a44d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a44d0-115">-DefaultProfile</span></span>
<span data-ttu-id="a44d0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a44d0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a44d0-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a44d0-117">-Name</span></span>
<span data-ttu-id="a44d0-118">Указывает имя HTTP-параметров серверной части, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a44d0-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a44d0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a44d0-119">CommonParameters</span></span>
<span data-ttu-id="a44d0-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a44d0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a44d0-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a44d0-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a44d0-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a44d0-122">INPUTS</span></span>

### <span data-ttu-id="a44d0-123">System. String</span><span class="sxs-lookup"><span data-stu-id="a44d0-123">System.String</span></span>

## <span data-ttu-id="a44d0-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a44d0-124">OUTPUTS</span></span>

### <span data-ttu-id="a44d0-125">Microsoft. Azure. Commands. Network. Models. AzureApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="a44d0-125">Microsoft.Azure.Commands.Network.Models.AzureApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="a44d0-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="a44d0-126">NOTES</span></span>

## <span data-ttu-id="a44d0-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a44d0-127">RELATED LINKS</span></span>

[<span data-ttu-id="a44d0-128">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a44d0-128">Add-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="a44d0-129">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a44d0-129">New-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="a44d0-130">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a44d0-130">Remove-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="a44d0-131">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a44d0-131">Set-AzApplicationGatewayBackendHttpSetting</span></span>]()

