---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 128AD64D-709A-4B59-B233-4221A9120AE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4803fd24952066c4dcea72daaf0c999b64ae4c5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076497"
---
# <span data-ttu-id="ddcbe-101">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ddcbe-101">Remove-AzureApplicationGateway</span></span>

## <span data-ttu-id="ddcbe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ddcbe-102">SYNOPSIS</span></span>
<span data-ttu-id="ddcbe-103">Удаляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="ddcbe-103">Removes an application gateway.</span></span>

## <span data-ttu-id="ddcbe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ddcbe-104">SYNTAX</span></span>

```
Remove-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ddcbe-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddcbe-105">DESCRIPTION</span></span>
<span data-ttu-id="ddcbe-106">Командлет **Remove-AzureApplicationGateway** удаляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="ddcbe-106">The **Remove-AzureApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="ddcbe-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ddcbe-107">EXAMPLES</span></span>

### <span data-ttu-id="ddcbe-108">Пример 1: Удаление шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="ddcbe-108">Example 1: Remove an application gateway</span></span>
```
PS C:\> Remove-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="ddcbe-109">Эта команда удаляет шлюз приложения с именем ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="ddcbe-109">This command removes the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="ddcbe-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ddcbe-110">PARAMETERS</span></span>

### <span data-ttu-id="ddcbe-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ddcbe-111">-Name</span></span>
<span data-ttu-id="ddcbe-112">Указывает имя шлюза приложений, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="ddcbe-112">Specifies the name of the application gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ddcbe-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="ddcbe-113">-Profile</span></span>
<span data-ttu-id="ddcbe-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ddcbe-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="ddcbe-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ddcbe-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ddcbe-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddcbe-116">CommonParameters</span></span>
<span data-ttu-id="ddcbe-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ddcbe-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddcbe-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddcbe-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddcbe-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ddcbe-119">INPUTS</span></span>

### <span data-ttu-id="ddcbe-120">System. String</span><span class="sxs-lookup"><span data-stu-id="ddcbe-120">System.String</span></span>

## <span data-ttu-id="ddcbe-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddcbe-121">OUTPUTS</span></span>

### <span data-ttu-id="ddcbe-122">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ddcbe-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="ddcbe-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="ddcbe-123">NOTES</span></span>

## <span data-ttu-id="ddcbe-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ddcbe-124">RELATED LINKS</span></span>

[<span data-ttu-id="ddcbe-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ddcbe-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="ddcbe-126">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ddcbe-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="ddcbe-127">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ddcbe-127">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="ddcbe-128">Остановить-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ddcbe-128">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="ddcbe-129">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ddcbe-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)


