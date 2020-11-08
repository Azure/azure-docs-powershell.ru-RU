---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2664607C-FF95-4EB7-869E-A421343B0517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 231f24a20471d8a4639b091c10d0e04f65b71b76
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075599"
---
# <span data-ttu-id="288e4-101">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="288e4-101">Get-AzureServiceExtension</span></span>

## <span data-ttu-id="288e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="288e4-102">SYNOPSIS</span></span>
<span data-ttu-id="288e4-103">Возвращает расширения облачной службы, применяемые к развертыванию.</span><span class="sxs-lookup"><span data-stu-id="288e4-103">Gets cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="288e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="288e4-104">SYNTAX</span></span>

```
Get-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-ExtensionName] <String>]
 [[-ProviderNamespace] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="288e4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="288e4-105">DESCRIPTION</span></span>
<span data-ttu-id="288e4-106">Командлет **Get-AzureServiceExtension** получает расширения для существующих облачных служб, применяемые к развертыванию.</span><span class="sxs-lookup"><span data-stu-id="288e4-106">The **Get-AzureServiceExtension** cmdlet gets existing cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="288e4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="288e4-107">EXAMPLES</span></span>

### <span data-ttu-id="288e4-108">Пример 1: получение указанного расширения</span><span class="sxs-lookup"><span data-stu-id="288e4-108">Example 1: Get a specified extension</span></span>
```
PS C:\> Get-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions"
```

<span data-ttu-id="288e4-109">Эта команда получает расширение облачной службы с указанным именем и пространством имен.</span><span class="sxs-lookup"><span data-stu-id="288e4-109">This command gets the cloud service extension with the specified name and namespace.</span></span>

## <span data-ttu-id="288e4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="288e4-110">PARAMETERS</span></span>

### <span data-ttu-id="288e4-111">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="288e4-111">-ExtensionName</span></span>
<span data-ttu-id="288e4-112">Задает имя расширения.</span><span class="sxs-lookup"><span data-stu-id="288e4-112">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="288e4-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="288e4-113">-InformationAction</span></span>
<span data-ttu-id="288e4-114">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="288e4-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="288e4-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="288e4-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="288e4-116">Продолжал</span><span class="sxs-lookup"><span data-stu-id="288e4-116">Continue</span></span>
- <span data-ttu-id="288e4-117">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="288e4-117">Ignore</span></span>
- <span data-ttu-id="288e4-118">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="288e4-118">Inquire</span></span>
- <span data-ttu-id="288e4-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="288e4-119">SilentlyContinue</span></span>
- <span data-ttu-id="288e4-120">Остановить</span><span class="sxs-lookup"><span data-stu-id="288e4-120">Stop</span></span>
- <span data-ttu-id="288e4-121">Рвать</span><span class="sxs-lookup"><span data-stu-id="288e4-121">Suspend</span></span>

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

### <span data-ttu-id="288e4-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="288e4-122">-InformationVariable</span></span>
<span data-ttu-id="288e4-123">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="288e4-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="288e4-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="288e4-124">-Profile</span></span>
<span data-ttu-id="288e4-125">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="288e4-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="288e4-126">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="288e4-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="288e4-127">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="288e4-127">-ProviderNamespace</span></span>
<span data-ttu-id="288e4-128">Задает пространство имен поставщика расширений.</span><span class="sxs-lookup"><span data-stu-id="288e4-128">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="288e4-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="288e4-129">-ServiceName</span></span>
<span data-ttu-id="288e4-130">Указывает имя службы Azure для развертывания.</span><span class="sxs-lookup"><span data-stu-id="288e4-130">Specifies the Azure service name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="288e4-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="288e4-131">-Slot</span></span>
<span data-ttu-id="288e4-132">Указывает среду развертывания.</span><span class="sxs-lookup"><span data-stu-id="288e4-132">Specifies the deployment environment.</span></span>
<span data-ttu-id="288e4-133">Допустимые значения этого параметра: "производственный" или "промежуточный".</span><span class="sxs-lookup"><span data-stu-id="288e4-133">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="288e4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="288e4-134">CommonParameters</span></span>
<span data-ttu-id="288e4-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="288e4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="288e4-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="288e4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="288e4-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="288e4-137">INPUTS</span></span>

## <span data-ttu-id="288e4-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="288e4-138">OUTPUTS</span></span>

## <span data-ttu-id="288e4-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="288e4-139">NOTES</span></span>

## <span data-ttu-id="288e4-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="288e4-140">RELATED LINKS</span></span>

[<span data-ttu-id="288e4-141">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="288e4-141">Remove-AzureServiceExtension</span></span>](./Remove-AzureServiceExtension.md)

[<span data-ttu-id="288e4-142">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="288e4-142">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


