---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 895F9A5F-D48F-403D-BD8F-72D72D420690
online version: ''
schema: 2.0.0
ms.openlocfilehash: 97bb3e07f5c6df25e7c03c167cc4cb49c25f9414
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075787"
---
# <span data-ttu-id="bbe1b-101">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="bbe1b-101">Set-AzureVNetConfig</span></span>

## <span data-ttu-id="bbe1b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bbe1b-102">SYNOPSIS</span></span>
<span data-ttu-id="bbe1b-103">Обновляет параметры виртуальной сети для облачной службы Azure.</span><span class="sxs-lookup"><span data-stu-id="bbe1b-103">Updates the virtual network settings for an Azure cloud service.</span></span>

## <span data-ttu-id="bbe1b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bbe1b-104">SYNTAX</span></span>

```
Set-AzureVNetConfig [-ConfigurationPath] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bbe1b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbe1b-105">DESCRIPTION</span></span>
<span data-ttu-id="bbe1b-106">Командлет **Set-AzureVNetConfig** обновляет конфигурацию сети для текущей подписки Azure, указав путь к файлу конфигурации сети (netcfg).</span><span class="sxs-lookup"><span data-stu-id="bbe1b-106">The **Set-AzureVNetConfig** cmdlet updates the network configuration for the current Azure subscription by specifying a path to a network configuration file (.netcfg).</span></span>
<span data-ttu-id="bbe1b-107">Файл конфигурации сети определяет DNS-серверы и подсети для облачных служб в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="bbe1b-107">The network configuration file defines DNS servers and subnets for cloud services within a subscription.</span></span>

## <span data-ttu-id="bbe1b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bbe1b-108">EXAMPLES</span></span>

### <span data-ttu-id="bbe1b-109">Пример 1: Обновление конфигурации сети подписки Azure на локальный файл</span><span class="sxs-lookup"><span data-stu-id="bbe1b-109">Example 1: Update the network configuration of the Azure subscription to a local file</span></span>
```
PS C:\> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="bbe1b-110">Эта команда обновляет сетевую конфигурацию текущей подписки Microsoft Azure на то, что она находится в локальном файле "c:\temp\MyAzNets.netcfg".</span><span class="sxs-lookup"><span data-stu-id="bbe1b-110">This command updates the network configuration of the current Microsoft Azure subscription to that in the local file "c:\temp\MyAzNets.netcfg".</span></span>

### <span data-ttu-id="bbe1b-111">Пример 2: Настройка подписки Azure и обновление конфигурации сети</span><span class="sxs-lookup"><span data-stu-id="bbe1b-111">Example 2: Set the Azure subscription and then update the network configuration</span></span>
```
PS C:\> $SubsId = "5bea2bc2-88a5-44b8-abe1-3e76733b6783"
C:\PS> $Cert = Get-Item cert:\LocalMachine\MY\82F105B2DA81149204A6257A9A91EC452B8C52C3
C:\PS> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="bbe1b-112">Этот пример задает подписку Microsoft Azure, а затем обновляет конфигурацию сети для этой подписки, используя конфигурацию, определенную в локальном файле "c:\temp\MyAzNets.netcfg".</span><span class="sxs-lookup"><span data-stu-id="bbe1b-112">This example sets the Microsoft Azure subscription, and then updates the network configuration of that subscription using the configuration defined in the local file "c:\temp\MyAzNets.netcfg".</span></span>

## <span data-ttu-id="bbe1b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bbe1b-113">PARAMETERS</span></span>

### <span data-ttu-id="bbe1b-114">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="bbe1b-114">-ConfigurationPath</span></span>
<span data-ttu-id="bbe1b-115">Указывает путь и имя файла конфигурации сети (netcfg).</span><span class="sxs-lookup"><span data-stu-id="bbe1b-115">Specifies the path and file name of a network configuration file (.netcfg).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe1b-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bbe1b-116">-InformationAction</span></span>
<span data-ttu-id="bbe1b-117">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="bbe1b-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bbe1b-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bbe1b-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bbe1b-119">Продолжал</span><span class="sxs-lookup"><span data-stu-id="bbe1b-119">Continue</span></span>
- <span data-ttu-id="bbe1b-120">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="bbe1b-120">Ignore</span></span>
- <span data-ttu-id="bbe1b-121">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="bbe1b-121">Inquire</span></span>
- <span data-ttu-id="bbe1b-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bbe1b-122">SilentlyContinue</span></span>
- <span data-ttu-id="bbe1b-123">Остановить</span><span class="sxs-lookup"><span data-stu-id="bbe1b-123">Stop</span></span>
- <span data-ttu-id="bbe1b-124">Рвать</span><span class="sxs-lookup"><span data-stu-id="bbe1b-124">Suspend</span></span>

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

### <span data-ttu-id="bbe1b-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bbe1b-125">-InformationVariable</span></span>
<span data-ttu-id="bbe1b-126">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="bbe1b-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bbe1b-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="bbe1b-127">-Profile</span></span>
<span data-ttu-id="bbe1b-128">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bbe1b-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bbe1b-129">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bbe1b-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bbe1b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbe1b-130">CommonParameters</span></span>
<span data-ttu-id="bbe1b-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bbe1b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbe1b-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbe1b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbe1b-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bbe1b-133">INPUTS</span></span>

## <span data-ttu-id="bbe1b-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbe1b-134">OUTPUTS</span></span>

## <span data-ttu-id="bbe1b-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="bbe1b-135">NOTES</span></span>

## <span data-ttu-id="bbe1b-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bbe1b-136">RELATED LINKS</span></span>

[<span data-ttu-id="bbe1b-137">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="bbe1b-137">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="bbe1b-138">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="bbe1b-138">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="bbe1b-139">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="bbe1b-139">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)


