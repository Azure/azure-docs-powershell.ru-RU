---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3F3BC5AF-8D7B-40BF-A072-A11C7BDCB6B3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09adc7e9b2faf9b9a905fa1c94fb6526e02c110f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075786"
---
# <span data-ttu-id="46f48-101">Set-AzureWalkUpgradeDomain</span><span class="sxs-lookup"><span data-stu-id="46f48-101">Set-AzureWalkUpgradeDomain</span></span>

## <span data-ttu-id="46f48-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="46f48-102">SYNOPSIS</span></span>
<span data-ttu-id="46f48-103">Просматривает указанный домен обновления.</span><span class="sxs-lookup"><span data-stu-id="46f48-103">Walks the specified upgrade domain.</span></span>

## <span data-ttu-id="46f48-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="46f48-104">SYNTAX</span></span>

```
Set-AzureWalkUpgradeDomain [-ServiceName] <String> [-Slot] <String> [-DomainNumber] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="46f48-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46f48-105">DESCRIPTION</span></span>
<span data-ttu-id="46f48-106">Командлет **Set-AzureWalkUpgradeDomain** инициирует фактическое обновление развертывания Azure.</span><span class="sxs-lookup"><span data-stu-id="46f48-106">The **Set-AzureWalkUpgradeDomain** cmdlet initiates the actual upgrade of an Azure deployment.</span></span>
<span data-ttu-id="46f48-107">Пакет и Конфигурация обновления задаются с помощью командлета **Set-AzureDeployment** с параметром-Upgrade.</span><span class="sxs-lookup"><span data-stu-id="46f48-107">The upgrade package and configuration are set by using the **Set-AzureDeployment** cmdlet with the -Upgrade switch.</span></span>

## <span data-ttu-id="46f48-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="46f48-108">EXAMPLES</span></span>

### <span data-ttu-id="46f48-109">Пример 1: Начало обновления рабочего развертывания</span><span class="sxs-lookup"><span data-stu-id="46f48-109">Example 1: Initiate an upgrade of a production deployment</span></span>
```
PS C:\> Set-AzureWalkUpgradeDomain -ServiceName "MySvc1" -slot "Production" -UpgradeDomain 2
```

<span data-ttu-id="46f48-110">Эта команда запускает обновление домена 2 для рабочего развертывания службы MySvc1.</span><span class="sxs-lookup"><span data-stu-id="46f48-110">This command initiates the upgrade of Upgrade Domain 2 of the production deployment of the MySvc1 service.</span></span>

## <span data-ttu-id="46f48-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="46f48-111">PARAMETERS</span></span>

### <span data-ttu-id="46f48-112">-DomainNumber</span><span class="sxs-lookup"><span data-stu-id="46f48-112">-DomainNumber</span></span>
<span data-ttu-id="46f48-113">Задает домен обновления для обновления.</span><span class="sxs-lookup"><span data-stu-id="46f48-113">Specifies the upgrade domain to upgrade.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f48-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="46f48-114">-InformationAction</span></span>
<span data-ttu-id="46f48-115">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="46f48-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="46f48-116">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="46f48-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="46f48-117">Продолжал</span><span class="sxs-lookup"><span data-stu-id="46f48-117">Continue</span></span>
- <span data-ttu-id="46f48-118">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="46f48-118">Ignore</span></span>
- <span data-ttu-id="46f48-119">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="46f48-119">Inquire</span></span>
- <span data-ttu-id="46f48-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="46f48-120">SilentlyContinue</span></span>
- <span data-ttu-id="46f48-121">Остановить</span><span class="sxs-lookup"><span data-stu-id="46f48-121">Stop</span></span>
- <span data-ttu-id="46f48-122">Рвать</span><span class="sxs-lookup"><span data-stu-id="46f48-122">Suspend</span></span>

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

### <span data-ttu-id="46f48-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="46f48-123">-InformationVariable</span></span>
<span data-ttu-id="46f48-124">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="46f48-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="46f48-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="46f48-125">-Profile</span></span>
<span data-ttu-id="46f48-126">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="46f48-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="46f48-127">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="46f48-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="46f48-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="46f48-128">-ServiceName</span></span>
<span data-ttu-id="46f48-129">Указывает имя службы Microsoft Azure для обновления.</span><span class="sxs-lookup"><span data-stu-id="46f48-129">Specifies the Microsoft Azure service name to upgrade.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f48-130">-Slot</span><span class="sxs-lookup"><span data-stu-id="46f48-130">-Slot</span></span>
<span data-ttu-id="46f48-131">Задает среду развертывания для обновления.</span><span class="sxs-lookup"><span data-stu-id="46f48-131">Specifies the environment of the deployment to upgrade.</span></span>

<span data-ttu-id="46f48-132">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="46f48-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="46f48-133">Промежуточного хранения</span><span class="sxs-lookup"><span data-stu-id="46f48-133">Staging</span></span>
- <span data-ttu-id="46f48-134">Спецификации</span><span class="sxs-lookup"><span data-stu-id="46f48-134">Production</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f48-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46f48-135">CommonParameters</span></span>
<span data-ttu-id="46f48-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="46f48-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46f48-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46f48-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46f48-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="46f48-138">INPUTS</span></span>

## <span data-ttu-id="46f48-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="46f48-139">OUTPUTS</span></span>

### <span data-ttu-id="46f48-140">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="46f48-140">ManagementOperationContext</span></span>

## <span data-ttu-id="46f48-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="46f48-141">NOTES</span></span>

## <span data-ttu-id="46f48-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46f48-142">RELATED LINKS</span></span>

[<span data-ttu-id="46f48-143">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="46f48-143">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


