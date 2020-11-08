---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 54C89A5F-BF94-468C-92E7-224808FDD0EC
online version: ''
schema: 2.0.0
ms.openlocfilehash: be84995e4826b79befc6282133d70f3ee4a79b4f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076227"
---
# <span data-ttu-id="4f9c2-101">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="4f9c2-101">New-AzureAffinityGroup</span></span>

## <span data-ttu-id="4f9c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4f9c2-102">SYNOPSIS</span></span>
<span data-ttu-id="4f9c2-103">Создает территориальную группу в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="4f9c2-103">Creates an affinity group in the current subscription.</span></span>

## <span data-ttu-id="4f9c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4f9c2-104">SYNTAX</span></span>

```
New-AzureAffinityGroup [-Name] <String> [-Label <String>] [-Description <String>] -Location <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f9c2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f9c2-105">DESCRIPTION</span></span>
<span data-ttu-id="4f9c2-106">Командлет **New-AzureAffinityGroup** создает территориальную группу Azure в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="4f9c2-106">The **New-AzureAffinityGroup** cmdlet creates an Azure affinity group in the current Azure subscription.</span></span>

<span data-ttu-id="4f9c2-107">Территориальная группа помещает ваши услуги и их ресурсы вместе в центр обработки данных Azure.</span><span class="sxs-lookup"><span data-stu-id="4f9c2-107">An affinity group puts your services and their resources together in an Azure datacenter.</span></span>
<span data-ttu-id="4f9c2-108">Для обеспечения оптимальной производительности групповая территориальная группа взаимодействуют между участниками.</span><span class="sxs-lookup"><span data-stu-id="4f9c2-108">The affinity group groups members together for optimal performance.</span></span>
<span data-ttu-id="4f9c2-109">Определение территориальных групп на уровне подписок.</span><span class="sxs-lookup"><span data-stu-id="4f9c2-109">Define affinity groups at the subscription level.</span></span>
<span data-ttu-id="4f9c2-110">Ваши территориальные группы доступны для всех последующих облачных служб или учетных записей хранения, которые вы создаете.</span><span class="sxs-lookup"><span data-stu-id="4f9c2-110">Your affinity groups are available to any subsequent cloud services or storage accounts that you create.</span></span>
<span data-ttu-id="4f9c2-111">Вы можете добавлять службы в территориальную группу только при ее создании.</span><span class="sxs-lookup"><span data-stu-id="4f9c2-111">You can add services to an affinity group only when you create it.</span></span>

## <span data-ttu-id="4f9c2-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4f9c2-112">EXAMPLES</span></span>

### <span data-ttu-id="4f9c2-113">Пример 1: создание территориальной группы</span><span class="sxs-lookup"><span data-stu-id="4f9c2-113">Example 1: Create an affinity group</span></span>
```
PS C:\> New-AzureAffinityGroup -Name "South01" -Location "South Central US" -Label "South Region" -Description "Affinity group for production applications in southern region."
```

<span data-ttu-id="4f9c2-114">Эта команда создает территориальную группу с именем South01 в Южной Центральной области США.</span><span class="sxs-lookup"><span data-stu-id="4f9c2-114">This command creates an affinity group named South01 in the South Central US region.</span></span>
<span data-ttu-id="4f9c2-115">Команда задает метку и описание.</span><span class="sxs-lookup"><span data-stu-id="4f9c2-115">The command specifies a label and a description.</span></span>

## <span data-ttu-id="4f9c2-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4f9c2-116">PARAMETERS</span></span>

### <span data-ttu-id="4f9c2-117">-Описание</span><span class="sxs-lookup"><span data-stu-id="4f9c2-117">-Description</span></span>
<span data-ttu-id="4f9c2-118">Задает описание территориальной группы.</span><span class="sxs-lookup"><span data-stu-id="4f9c2-118">Specifies a description for the affinity group.</span></span>
<span data-ttu-id="4f9c2-119">Описание может иметь длину до 1024 символов.</span><span class="sxs-lookup"><span data-stu-id="4f9c2-119">The description may be up to 1024 characters long.</span></span>

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

### <span data-ttu-id="4f9c2-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4f9c2-120">-InformationAction</span></span>
<span data-ttu-id="4f9c2-121">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="4f9c2-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4f9c2-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4f9c2-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4f9c2-123">Продолжал</span><span class="sxs-lookup"><span data-stu-id="4f9c2-123">Continue</span></span>
- <span data-ttu-id="4f9c2-124">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="4f9c2-124">Ignore</span></span>
- <span data-ttu-id="4f9c2-125">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="4f9c2-125">Inquire</span></span>
- <span data-ttu-id="4f9c2-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4f9c2-126">SilentlyContinue</span></span>
- <span data-ttu-id="4f9c2-127">Остановить</span><span class="sxs-lookup"><span data-stu-id="4f9c2-127">Stop</span></span>
- <span data-ttu-id="4f9c2-128">Рвать</span><span class="sxs-lookup"><span data-stu-id="4f9c2-128">Suspend</span></span>

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

### <span data-ttu-id="4f9c2-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4f9c2-129">-InformationVariable</span></span>
<span data-ttu-id="4f9c2-130">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="4f9c2-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4f9c2-131">-Label</span><span class="sxs-lookup"><span data-stu-id="4f9c2-131">-Label</span></span>
<span data-ttu-id="4f9c2-132">Указывает метку для территориальной группы.</span><span class="sxs-lookup"><span data-stu-id="4f9c2-132">Specifies a label for the affinity group.</span></span>
<span data-ttu-id="4f9c2-133">Метка может иметь длину до 100 символов.</span><span class="sxs-lookup"><span data-stu-id="4f9c2-133">The label may be up to 100 characters long.</span></span>

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

### <span data-ttu-id="4f9c2-134">-Location</span><span class="sxs-lookup"><span data-stu-id="4f9c2-134">-Location</span></span>
<span data-ttu-id="4f9c2-135">Указывает географическое расположение центра обработки данных Azure, в котором этот командлет создает территориальную группу.</span><span class="sxs-lookup"><span data-stu-id="4f9c2-135">Specifies the geographical location of the Azure datacenter where this cmdlet creates the affinity group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f9c2-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4f9c2-136">-Name</span></span>
<span data-ttu-id="4f9c2-137">Задает имя для территориальной группы.</span><span class="sxs-lookup"><span data-stu-id="4f9c2-137">Specifies a name for the affinity group.</span></span>
<span data-ttu-id="4f9c2-138">Имя должно быть уникальным для подписки.</span><span class="sxs-lookup"><span data-stu-id="4f9c2-138">The name must be unique to the subscription.</span></span>

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

### <span data-ttu-id="4f9c2-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="4f9c2-139">-Profile</span></span>
<span data-ttu-id="4f9c2-140">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4f9c2-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4f9c2-141">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4f9c2-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4f9c2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f9c2-142">CommonParameters</span></span>
<span data-ttu-id="4f9c2-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4f9c2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f9c2-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f9c2-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f9c2-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4f9c2-145">INPUTS</span></span>

## <span data-ttu-id="4f9c2-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f9c2-146">OUTPUTS</span></span>

## <span data-ttu-id="4f9c2-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="4f9c2-147">NOTES</span></span>

## <span data-ttu-id="4f9c2-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f9c2-148">RELATED LINKS</span></span>

[<span data-ttu-id="4f9c2-149">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="4f9c2-149">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="4f9c2-150">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="4f9c2-150">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)

[<span data-ttu-id="4f9c2-151">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="4f9c2-151">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


