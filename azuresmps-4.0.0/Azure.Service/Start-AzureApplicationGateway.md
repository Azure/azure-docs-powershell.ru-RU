---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D50984B7-FD97-4713-8E56-1C06D2B008E3
online version: ''
schema: 2.0.0
ms.openlocfilehash: a01d59d6a0755b3763eaef9b7532326ca0ffd402
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075779"
---
# <span data-ttu-id="74d0e-101">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74d0e-101">Start-AzureApplicationGateway</span></span>

## <span data-ttu-id="74d0e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74d0e-102">SYNOPSIS</span></span>
<span data-ttu-id="74d0e-103">Запускает шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="74d0e-103">Starts an application gateway.</span></span>

## <span data-ttu-id="74d0e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74d0e-104">SYNTAX</span></span>

```
Start-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="74d0e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74d0e-105">DESCRIPTION</span></span>
<span data-ttu-id="74d0e-106">Командлет **Start-AzureApplicationGateway** запускает шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="74d0e-106">The **Start-AzureApplicationGateway** cmdlet starts an application gateway.</span></span>

## <span data-ttu-id="74d0e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74d0e-107">EXAMPLES</span></span>

### <span data-ttu-id="74d0e-108">Пример 1: запуск шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="74d0e-108">Example 1: Start an application gateway</span></span>
```
PS C:\> Start-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="74d0e-109">Эта команда запускает шлюз приложений с именем ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="74d0e-109">This command starts the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="74d0e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74d0e-110">PARAMETERS</span></span>

### <span data-ttu-id="74d0e-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="74d0e-111">-Name</span></span>
<span data-ttu-id="74d0e-112">Указывает имя шлюза приложения, который запускается этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="74d0e-112">Specifies the name of the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="74d0e-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="74d0e-113">-Profile</span></span>
<span data-ttu-id="74d0e-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="74d0e-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="74d0e-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="74d0e-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="74d0e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74d0e-116">CommonParameters</span></span>
<span data-ttu-id="74d0e-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74d0e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74d0e-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74d0e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74d0e-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74d0e-119">INPUTS</span></span>

### <span data-ttu-id="74d0e-120">System. String</span><span class="sxs-lookup"><span data-stu-id="74d0e-120">System.String</span></span>

## <span data-ttu-id="74d0e-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74d0e-121">OUTPUTS</span></span>

### <span data-ttu-id="74d0e-122">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="74d0e-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="74d0e-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="74d0e-123">NOTES</span></span>

## <span data-ttu-id="74d0e-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74d0e-124">RELATED LINKS</span></span>

[<span data-ttu-id="74d0e-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74d0e-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="74d0e-126">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74d0e-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="74d0e-127">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74d0e-127">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="74d0e-128">Остановить-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74d0e-128">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="74d0e-129">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74d0e-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)


