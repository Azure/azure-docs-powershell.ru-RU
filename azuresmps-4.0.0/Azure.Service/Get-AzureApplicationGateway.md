---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 0AED21E8-A638-4019-9B23-447472E56C7A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 202066cfc2649b0f56810123e211bbeb5d69720f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075670"
---
# <span data-ttu-id="05648-101">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="05648-101">Get-AzureApplicationGateway</span></span>

## <span data-ttu-id="05648-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="05648-102">SYNOPSIS</span></span>
<span data-ttu-id="05648-103">Получает шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="05648-103">Gets an Application Gateway.</span></span>

## <span data-ttu-id="05648-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="05648-104">SYNTAX</span></span>

```
Get-AzureApplicationGateway [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="05648-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05648-105">DESCRIPTION</span></span>
<span data-ttu-id="05648-106">Командлет **Get-AzureApplicationGateway** получает существующий шлюз приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="05648-106">The **Get-AzureApplicationGateway** cmdlet gets an existing Azure Application Gateway.</span></span>

## <span data-ttu-id="05648-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="05648-107">EXAMPLES</span></span>

### <span data-ttu-id="05648-108">Пример 1: получение шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="05648-108">Example 1: Get an Application Gateway</span></span>
```
PS C:\> Get-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="05648-109">Эта команда получает шлюз приложения с именем ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="05648-109">This command gets the Application Gateway named ApplicationGateway06.</span></span>

### <span data-ttu-id="05648-110">Пример 2: получение всех шлюзов приложений</span><span class="sxs-lookup"><span data-stu-id="05648-110">Example 2: Get all Application Gateways</span></span>
```
PS C:\> Get-AzureApplicationGateway
```

<span data-ttu-id="05648-111">Эта команда получает список всех шлюзов приложений для вашей подписки.</span><span class="sxs-lookup"><span data-stu-id="05648-111">This command gets all the Application Gateways under your subscription.</span></span>

## <span data-ttu-id="05648-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="05648-112">PARAMETERS</span></span>

### <span data-ttu-id="05648-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="05648-113">-Name</span></span>
<span data-ttu-id="05648-114">Указывает имя шлюза приложения, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="05648-114">Specifies the name of the Application Gateway that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05648-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="05648-115">-Profile</span></span>
<span data-ttu-id="05648-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="05648-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="05648-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="05648-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="05648-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05648-118">CommonParameters</span></span>
<span data-ttu-id="05648-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="05648-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05648-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05648-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05648-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="05648-121">INPUTS</span></span>

### <span data-ttu-id="05648-122">System. String</span><span class="sxs-lookup"><span data-stu-id="05648-122">System.String</span></span>

## <span data-ttu-id="05648-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="05648-123">OUTPUTS</span></span>

### <span data-ttu-id="05648-124">Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGateway, IEnumerable<Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGateway></span><span class="sxs-lookup"><span data-stu-id="05648-124">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGateway, IEnumerable<Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGateway></span></span>

## <span data-ttu-id="05648-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="05648-125">NOTES</span></span>

## <span data-ttu-id="05648-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05648-126">RELATED LINKS</span></span>

[<span data-ttu-id="05648-127">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="05648-127">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="05648-128">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="05648-128">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="05648-129">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="05648-129">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="05648-130">Остановить-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="05648-130">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="05648-131">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="05648-131">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)


