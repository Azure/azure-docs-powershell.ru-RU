---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 17BA2ED5-E347-45C0-AF20-CDD288469514
online version: ''
schema: 2.0.0
ms.openlocfilehash: a07afcadb2207f2e4377601abfa6094bc3293328
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076408"
---
# <span data-ttu-id="9c237-101">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c237-101">Stop-AzureApplicationGateway</span></span>

## <span data-ttu-id="9c237-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c237-102">SYNOPSIS</span></span>
<span data-ttu-id="9c237-103">Останавливает работу шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="9c237-103">Stops an application gateway.</span></span>

## <span data-ttu-id="9c237-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c237-104">SYNTAX</span></span>

```
Stop-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9c237-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c237-105">DESCRIPTION</span></span>
<span data-ttu-id="9c237-106">Командлет **Stop-AzureApplicationGateway** останавливает работу шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="9c237-106">The **Stop-AzureApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="9c237-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c237-107">EXAMPLES</span></span>

### <span data-ttu-id="9c237-108">Пример 1: остановка шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="9c237-108">Example 1: Stop an application gateway</span></span>
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="9c237-109">Эта команда останавливает шлюз приложений с именем ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="9c237-109">This command stops the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="9c237-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c237-110">PARAMETERS</span></span>

### <span data-ttu-id="9c237-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9c237-111">-Name</span></span>
<span data-ttu-id="9c237-112">Указывает имя шлюза приложений, который останавливается для этого командлета.</span><span class="sxs-lookup"><span data-stu-id="9c237-112">Specifies the name of the application gateway that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c237-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="9c237-113">-Profile</span></span>
<span data-ttu-id="9c237-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9c237-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9c237-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9c237-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c237-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c237-116">CommonParameters</span></span>
<span data-ttu-id="9c237-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c237-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c237-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c237-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c237-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c237-119">INPUTS</span></span>

### <span data-ttu-id="9c237-120">System. String</span><span class="sxs-lookup"><span data-stu-id="9c237-120">System.String</span></span>

## <span data-ttu-id="9c237-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c237-121">OUTPUTS</span></span>

### <span data-ttu-id="9c237-122">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9c237-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="9c237-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c237-123">NOTES</span></span>

## <span data-ttu-id="9c237-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c237-124">RELATED LINKS</span></span>

[<span data-ttu-id="9c237-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c237-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="9c237-126">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c237-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="9c237-127">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c237-127">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="9c237-128">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c237-128">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="9c237-129">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c237-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)
