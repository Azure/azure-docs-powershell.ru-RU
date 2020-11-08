---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F34910FA-B024-4C1C-B040-671C8962C49D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 558d714c432efd1dbd8f11feb09b0bbde035e2ff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076288"
---
# <span data-ttu-id="6f0dd-101">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="6f0dd-101">Get-AzureVNetConfig</span></span>

## <span data-ttu-id="6f0dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f0dd-102">SYNOPSIS</span></span>
<span data-ttu-id="6f0dd-103">Получает конфигурацию виртуальной сети Azure из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="6f0dd-103">Gets the Azure virtual network configuration from the current subscription.</span></span>

## <span data-ttu-id="6f0dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f0dd-104">SYNTAX</span></span>

```
Get-AzureVNetConfig [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6f0dd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f0dd-105">DESCRIPTION</span></span>
<span data-ttu-id="6f0dd-106">Командлет **Get-AzureVNetConfig** извлекает конфигурацию виртуальной сети для текущей подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="6f0dd-106">The **Get-AzureVNetConfig** cmdlet retrieves the virtual network configuration of the current Azure subscription.</span></span>
<span data-ttu-id="6f0dd-107">Если указан параметр *ExportToFile* , создается файл конфигурации сети.</span><span class="sxs-lookup"><span data-stu-id="6f0dd-107">If the *ExportToFile* parameter is specified, a network configuration file is created.</span></span>

## <span data-ttu-id="6f0dd-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f0dd-108">EXAMPLES</span></span>

### <span data-ttu-id="6f0dd-109">Пример 1: получение конфигурации виртуальной сети для текущей подписки Azure</span><span class="sxs-lookup"><span data-stu-id="6f0dd-109">Example 1: Get the virtual network configuration of a current Azure subscription</span></span>
```
PS C:\> Get-AzureVNetConfig
```

<span data-ttu-id="6f0dd-110">Эта команда возвращает конфигурацию виртуальной сети для текущей подписки Azure и отображает ее.</span><span class="sxs-lookup"><span data-stu-id="6f0dd-110">This command gets the virtual network configuration of the current Azure subscription and displays it.</span></span>

### <span data-ttu-id="6f0dd-111">Пример 2: получение конфигурации виртуальной сети для текущей подписки Azure и ее сохранение в локальном файле</span><span class="sxs-lookup"><span data-stu-id="6f0dd-111">Example 2: Get the virtual network configuration of the current Azure subscription and save it to a local file</span></span>
```
PS C:\> Get-AzureVNetConfig -ExportToFile "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="6f0dd-112">Эта команда возвращает конфигурацию виртуальной сети для текущей подписки Azure, а затем сохраняет ее в локальном файле.</span><span class="sxs-lookup"><span data-stu-id="6f0dd-112">This command gets the virtual network configuration of the current Azure subscription and then saves it to a local file.</span></span>

## <span data-ttu-id="6f0dd-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f0dd-113">PARAMETERS</span></span>

### <span data-ttu-id="6f0dd-114">-ExportToFile</span><span class="sxs-lookup"><span data-stu-id="6f0dd-114">-ExportToFile</span></span>
<span data-ttu-id="6f0dd-115">Указывает путь и имя файла конфигурации сети, который нужно создать на основе параметров.</span><span class="sxs-lookup"><span data-stu-id="6f0dd-115">Specifies the path and file name of a network configuration file to be created from the settings.</span></span>

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

### <span data-ttu-id="6f0dd-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6f0dd-116">-InformationAction</span></span>
<span data-ttu-id="6f0dd-117">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="6f0dd-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6f0dd-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6f0dd-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6f0dd-119">Продолжал</span><span class="sxs-lookup"><span data-stu-id="6f0dd-119">Continue</span></span>
- <span data-ttu-id="6f0dd-120">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="6f0dd-120">Ignore</span></span>
- <span data-ttu-id="6f0dd-121">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="6f0dd-121">Inquire</span></span>
- <span data-ttu-id="6f0dd-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6f0dd-122">SilentlyContinue</span></span>
- <span data-ttu-id="6f0dd-123">Остановить</span><span class="sxs-lookup"><span data-stu-id="6f0dd-123">Stop</span></span>
- <span data-ttu-id="6f0dd-124">Рвать</span><span class="sxs-lookup"><span data-stu-id="6f0dd-124">Suspend</span></span>

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

### <span data-ttu-id="6f0dd-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6f0dd-125">-InformationVariable</span></span>
<span data-ttu-id="6f0dd-126">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="6f0dd-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6f0dd-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="6f0dd-127">-Profile</span></span>
<span data-ttu-id="6f0dd-128">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6f0dd-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6f0dd-129">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6f0dd-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6f0dd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f0dd-130">CommonParameters</span></span>
<span data-ttu-id="6f0dd-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f0dd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f0dd-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f0dd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f0dd-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f0dd-133">INPUTS</span></span>

## <span data-ttu-id="6f0dd-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f0dd-134">OUTPUTS</span></span>

## <span data-ttu-id="6f0dd-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f0dd-135">NOTES</span></span>

## <span data-ttu-id="6f0dd-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f0dd-136">RELATED LINKS</span></span>

[<span data-ttu-id="6f0dd-137">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="6f0dd-137">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="6f0dd-138">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="6f0dd-138">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)

[<span data-ttu-id="6f0dd-139">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="6f0dd-139">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


