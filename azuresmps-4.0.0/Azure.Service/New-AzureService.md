---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BB216903-B2BB-4948-AC28-408ED6C768F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6cae249f99282006ff8636e8d727485a223e2a1d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075899"
---
# <span data-ttu-id="46185-101">New-AzureService</span><span class="sxs-lookup"><span data-stu-id="46185-101">New-AzureService</span></span>

## <span data-ttu-id="46185-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="46185-102">SYNOPSIS</span></span>
<span data-ttu-id="46185-103">Создает службу Azure.</span><span class="sxs-lookup"><span data-stu-id="46185-103">Creates an Azure service.</span></span>

## <span data-ttu-id="46185-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="46185-104">SYNTAX</span></span>

### <span data-ttu-id="46185-105">ParameterSetAffinityGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="46185-105">ParameterSetAffinityGroup (Default)</span></span>
```
New-AzureService [-ServiceName] <String> [-AffinityGroup] <String> [[-Label] <String>]
 [[-Description] <String>] [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="46185-106">ParameterSetLocation</span><span class="sxs-lookup"><span data-stu-id="46185-106">ParameterSetLocation</span></span>
```
New-AzureService [-ServiceName] <String> [-Location] <String> [[-Label] <String>] [[-Description] <String>]
 [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="46185-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46185-107">DESCRIPTION</span></span>
<span data-ttu-id="46185-108">Командлет **New-AzureService** создает новую службу Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="46185-108">The **New-AzureService** cmdlet creates a new Azure service in the current subscription.</span></span>

## <span data-ttu-id="46185-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="46185-109">EXAMPLES</span></span>

### <span data-ttu-id="46185-110">Пример 1: создание службы</span><span class="sxs-lookup"><span data-stu-id="46185-110">Example 1: Create a service</span></span>
```
PS C:\> New-AzureService -ServiceName "MySvc01" -Label "MyTestService" -Location "South Central US"
```

<span data-ttu-id="46185-111">Эта команда создает новую службу с именем MySvc01 в Южной Центральной области США.</span><span class="sxs-lookup"><span data-stu-id="46185-111">This command creates a new service named MySvc01 in the South Central US location.</span></span>

### <span data-ttu-id="46185-112">Пример 2: создание службы в территориальной группе</span><span class="sxs-lookup"><span data-stu-id="46185-112">Example 2: Create a service in an affinity group</span></span>
```
PS C:\> New-AzureService -ServiceName "MySvc01" -AffinityGroup NorthRegion
```

<span data-ttu-id="46185-113">Эта команда создает новую службу с именем MySvc01, используя территориальную группу NorthRegion.</span><span class="sxs-lookup"><span data-stu-id="46185-113">This command creates a new service named MySvc01 using the NorthRegion affinity group.</span></span>

## <span data-ttu-id="46185-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="46185-114">PARAMETERS</span></span>

### <span data-ttu-id="46185-115">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="46185-115">-AffinityGroup</span></span>
<span data-ttu-id="46185-116">Указывает территориальную группу, связанную с подпиской.</span><span class="sxs-lookup"><span data-stu-id="46185-116">Specifies the affinity group associated with the subscription.</span></span>
<span data-ttu-id="46185-117">Если параметр *Location* не задан, требуется указать территориальную группу.</span><span class="sxs-lookup"><span data-stu-id="46185-117">If you do not specify the *Location* parameter, an affinity group is required.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46185-118">-Описание</span><span class="sxs-lookup"><span data-stu-id="46185-118">-Description</span></span>
<span data-ttu-id="46185-119">Задает описание службы.</span><span class="sxs-lookup"><span data-stu-id="46185-119">Specifies a description for the service.</span></span>
<span data-ttu-id="46185-120">Описание может иметь длину до 1024 символов.</span><span class="sxs-lookup"><span data-stu-id="46185-120">The description may be up to 1024 characters in length.</span></span>

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

### <span data-ttu-id="46185-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="46185-121">-InformationAction</span></span>
<span data-ttu-id="46185-122">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="46185-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="46185-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="46185-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="46185-124">Продолжал</span><span class="sxs-lookup"><span data-stu-id="46185-124">Continue</span></span>
- <span data-ttu-id="46185-125">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="46185-125">Ignore</span></span>
- <span data-ttu-id="46185-126">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="46185-126">Inquire</span></span>
- <span data-ttu-id="46185-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="46185-127">SilentlyContinue</span></span>
- <span data-ttu-id="46185-128">Остановить</span><span class="sxs-lookup"><span data-stu-id="46185-128">Stop</span></span>
- <span data-ttu-id="46185-129">Рвать</span><span class="sxs-lookup"><span data-stu-id="46185-129">Suspend</span></span>

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

### <span data-ttu-id="46185-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="46185-130">-InformationVariable</span></span>
<span data-ttu-id="46185-131">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="46185-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="46185-132">-Label</span><span class="sxs-lookup"><span data-stu-id="46185-132">-Label</span></span>
<span data-ttu-id="46185-133">Указывает метку для службы.</span><span class="sxs-lookup"><span data-stu-id="46185-133">Specifies a label for the service.</span></span>
<span data-ttu-id="46185-134">Метка может иметь длину до 100 знаков.</span><span class="sxs-lookup"><span data-stu-id="46185-134">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46185-135">-Location</span><span class="sxs-lookup"><span data-stu-id="46185-135">-Location</span></span>
<span data-ttu-id="46185-136">Указывает расположение службы.</span><span class="sxs-lookup"><span data-stu-id="46185-136">Specifies the location for the service.</span></span>
<span data-ttu-id="46185-137">Расположение является обязательным, если не указана территориальная группа.</span><span class="sxs-lookup"><span data-stu-id="46185-137">A location is required if there isn't a specified Affinity Group.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetLocation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46185-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="46185-138">-Profile</span></span>
<span data-ttu-id="46185-139">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="46185-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="46185-140">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="46185-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="46185-141">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="46185-141">-ReverseDnsFqdn</span></span>
<span data-ttu-id="46185-142">Указывает полное доменное имя для обратного DNS-имени.</span><span class="sxs-lookup"><span data-stu-id="46185-142">Specifies the fully qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46185-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="46185-143">-ServiceName</span></span>
<span data-ttu-id="46185-144">Указывает имя новой службы.</span><span class="sxs-lookup"><span data-stu-id="46185-144">Specifies the name of the new service.</span></span>
<span data-ttu-id="46185-145">Имя должно быть уникальным для подписки.</span><span class="sxs-lookup"><span data-stu-id="46185-145">The name must be unique to the subscription.</span></span>

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

### <span data-ttu-id="46185-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46185-146">CommonParameters</span></span>
<span data-ttu-id="46185-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="46185-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46185-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46185-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46185-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="46185-149">INPUTS</span></span>

## <span data-ttu-id="46185-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="46185-150">OUTPUTS</span></span>

## <span data-ttu-id="46185-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="46185-151">NOTES</span></span>

## <span data-ttu-id="46185-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46185-152">RELATED LINKS</span></span>

[<span data-ttu-id="46185-153">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="46185-153">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="46185-154">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="46185-154">Set-AzureService</span></span>](./Set-AzureService.md)


