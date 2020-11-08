---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D903741F-1D22-48FC-BFA5-6876E557EFE5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4284d34ef5151dbcd16d9ed882dcf112abbb8ea5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075492"
---
# <span data-ttu-id="11624-101">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="11624-101">Remove-AzureVNetConfig</span></span>

## <span data-ttu-id="11624-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11624-102">SYNOPSIS</span></span>
<span data-ttu-id="11624-103">Удаление конфигурации сети из текущей подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="11624-103">Deletes the network configuration from the current Azure subscription.</span></span>

## <span data-ttu-id="11624-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11624-104">SYNTAX</span></span>

```
Remove-AzureVNetConfig [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="11624-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11624-105">DESCRIPTION</span></span>
<span data-ttu-id="11624-106">Командлет **Remove-AzureVNetConfig** удаляет все параметры виртуальной сети из текущей подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="11624-106">The **Remove-AzureVNetConfig** cmdlet removes all virtual network settings from the current Azure subscription.</span></span>

## <span data-ttu-id="11624-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11624-107">EXAMPLES</span></span>

### <span data-ttu-id="11624-108">Пример 1: Удаление конфигурации виртуальной сети из текущей подписки</span><span class="sxs-lookup"><span data-stu-id="11624-108">Example 1: Remove a virtual network configuration from the current subscription</span></span>
```
PS C:\> Remove-AzureVNetConfig
```

<span data-ttu-id="11624-109">Эта команда удаляет конфигурацию виртуальной сети из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="11624-109">This command removes the virtual network configuration from the current subscription.</span></span>

## <span data-ttu-id="11624-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11624-110">PARAMETERS</span></span>

### <span data-ttu-id="11624-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="11624-111">-InformationAction</span></span>
<span data-ttu-id="11624-112">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="11624-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="11624-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="11624-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="11624-114">Продолжал</span><span class="sxs-lookup"><span data-stu-id="11624-114">Continue</span></span>
- <span data-ttu-id="11624-115">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="11624-115">Ignore</span></span>
- <span data-ttu-id="11624-116">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="11624-116">Inquire</span></span>
- <span data-ttu-id="11624-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="11624-117">SilentlyContinue</span></span>
- <span data-ttu-id="11624-118">Остановить</span><span class="sxs-lookup"><span data-stu-id="11624-118">Stop</span></span>
- <span data-ttu-id="11624-119">Рвать</span><span class="sxs-lookup"><span data-stu-id="11624-119">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11624-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="11624-120">-InformationVariable</span></span>
<span data-ttu-id="11624-121">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="11624-121">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11624-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="11624-122">-Profile</span></span>
<span data-ttu-id="11624-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="11624-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="11624-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="11624-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="11624-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11624-125">CommonParameters</span></span>
<span data-ttu-id="11624-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="11624-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11624-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11624-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11624-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11624-128">INPUTS</span></span>

## <span data-ttu-id="11624-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11624-129">OUTPUTS</span></span>

## <span data-ttu-id="11624-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="11624-130">NOTES</span></span>

## <span data-ttu-id="11624-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11624-131">RELATED LINKS</span></span>

[<span data-ttu-id="11624-132">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="11624-132">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="11624-133">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="11624-133">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="11624-134">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="11624-134">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


