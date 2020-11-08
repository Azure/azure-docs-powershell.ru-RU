---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D08CB0A0-A0A9-4E0A-B1AB-A19A655B501B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5fd66813dcfc08f5e2f5276c4019443f9166945d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075596"
---
# <span data-ttu-id="12bc2-101">Get-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="12bc2-101">Get-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="12bc2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="12bc2-102">SYNOPSIS</span></span>
<span data-ttu-id="12bc2-103">Этот командлет получает расширение удаленного рабочего стола облачной службы, примененное ко всем ролям или именованным ролям в определенном слоте развертывания.</span><span class="sxs-lookup"><span data-stu-id="12bc2-103">This cmdlet gets the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="12bc2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="12bc2-104">SYNTAX</span></span>

```
Get-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="12bc2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12bc2-105">DESCRIPTION</span></span>
<span data-ttu-id="12bc2-106">Командлет **Get-AzureServiceRemoteDesktopExtension** получает расширение удаленного рабочего стола облачной службы, примененное ко всем ролям или именованным ролям в определенном слоте развертывания.</span><span class="sxs-lookup"><span data-stu-id="12bc2-106">The **Get-AzureServiceRemoteDesktopExtension** cmdlet gets the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="12bc2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="12bc2-107">EXAMPLES</span></span>

### <span data-ttu-id="12bc2-108">Пример 1: получение расширения удаленного рабочего стола для указанной службы</span><span class="sxs-lookup"><span data-stu-id="12bc2-108">Example 1: Get remote desktop extension for the specified service</span></span>
```
PS C:\> Get-AzureServiceRemoteDesktopExtension -ServiceName $svc
```

<span data-ttu-id="12bc2-109">Эта команда получает расширение удаленного рабочего стола для указанной службы.</span><span class="sxs-lookup"><span data-stu-id="12bc2-109">This command gets the remote desktop extension for the specified service.</span></span>

## <span data-ttu-id="12bc2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="12bc2-110">PARAMETERS</span></span>

### <span data-ttu-id="12bc2-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="12bc2-111">-InformationAction</span></span>
<span data-ttu-id="12bc2-112">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="12bc2-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="12bc2-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="12bc2-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="12bc2-114">Продолжал</span><span class="sxs-lookup"><span data-stu-id="12bc2-114">Continue</span></span>
- <span data-ttu-id="12bc2-115">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="12bc2-115">Ignore</span></span>
- <span data-ttu-id="12bc2-116">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="12bc2-116">Inquire</span></span>
- <span data-ttu-id="12bc2-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="12bc2-117">SilentlyContinue</span></span>
- <span data-ttu-id="12bc2-118">Остановить</span><span class="sxs-lookup"><span data-stu-id="12bc2-118">Stop</span></span>
- <span data-ttu-id="12bc2-119">Рвать</span><span class="sxs-lookup"><span data-stu-id="12bc2-119">Suspend</span></span>

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

### <span data-ttu-id="12bc2-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="12bc2-120">-InformationVariable</span></span>
<span data-ttu-id="12bc2-121">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="12bc2-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="12bc2-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="12bc2-122">-Profile</span></span>
<span data-ttu-id="12bc2-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="12bc2-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="12bc2-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="12bc2-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="12bc2-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="12bc2-125">-ServiceName</span></span>
<span data-ttu-id="12bc2-126">Указывает имя службы Azure для развертывания.</span><span class="sxs-lookup"><span data-stu-id="12bc2-126">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="12bc2-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="12bc2-127">-Slot</span></span>
<span data-ttu-id="12bc2-128">Задает среду развертывания, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="12bc2-128">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="12bc2-129">Допустимые значения этого параметра: "производственный" или "промежуточный".</span><span class="sxs-lookup"><span data-stu-id="12bc2-129">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="12bc2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12bc2-130">CommonParameters</span></span>
<span data-ttu-id="12bc2-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="12bc2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12bc2-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12bc2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12bc2-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="12bc2-133">INPUTS</span></span>

## <span data-ttu-id="12bc2-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="12bc2-134">OUTPUTS</span></span>

## <span data-ttu-id="12bc2-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="12bc2-135">NOTES</span></span>

## <span data-ttu-id="12bc2-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12bc2-136">RELATED LINKS</span></span>

[<span data-ttu-id="12bc2-137">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="12bc2-137">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


