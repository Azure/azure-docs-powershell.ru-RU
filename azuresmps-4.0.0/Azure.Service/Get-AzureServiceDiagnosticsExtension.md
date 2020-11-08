---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 235DD5D7-BE24-4FBE-88E2-40D1943ED155
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4fb3f35bc64a1431550d4da5aa669e934cd3a7f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075603"
---
# <span data-ttu-id="db9ae-101">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="db9ae-101">Get-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="db9ae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db9ae-102">SYNOPSIS</span></span>
<span data-ttu-id="db9ae-103">Получает расширение диагностики облачных служб, примененное для всех ролей или именованных ролей в определенном слоте развертывания.</span><span class="sxs-lookup"><span data-stu-id="db9ae-103">Gets the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="db9ae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db9ae-104">SYNTAX</span></span>

```
Get-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="db9ae-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db9ae-105">DESCRIPTION</span></span>
<span data-ttu-id="db9ae-106">Командлет **Get-AzureServiceDiagnosticsExtension** получает расширение диагностики облачной службы, примененное ко всем ролям или именованным ролям в определенном слоте развертывания.</span><span class="sxs-lookup"><span data-stu-id="db9ae-106">The **Get-AzureServiceDiagnosticsExtension** cmdlet gets the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="db9ae-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db9ae-107">EXAMPLES</span></span>

### <span data-ttu-id="db9ae-108">Пример 1: получение расширения диагностики служб</span><span class="sxs-lookup"><span data-stu-id="db9ae-108">Example 1: Get service diagnostics extension</span></span> 
```
PS C:\> Get-AzureServiceDiagnosticsExtension -ServiceName $Svc
```

<span data-ttu-id="db9ae-109">Эта команда получает диагностику службы для каждой роли.</span><span class="sxs-lookup"><span data-stu-id="db9ae-109">This command gets the service diagnostics for a service, across all roles.</span></span>

## <span data-ttu-id="db9ae-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db9ae-110">PARAMETERS</span></span>

### <span data-ttu-id="db9ae-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="db9ae-111">-InformationAction</span></span>
<span data-ttu-id="db9ae-112">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="db9ae-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="db9ae-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="db9ae-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="db9ae-114">Продолжал</span><span class="sxs-lookup"><span data-stu-id="db9ae-114">Continue</span></span>
- <span data-ttu-id="db9ae-115">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="db9ae-115">Ignore</span></span>
- <span data-ttu-id="db9ae-116">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="db9ae-116">Inquire</span></span>
- <span data-ttu-id="db9ae-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="db9ae-117">SilentlyContinue</span></span>
- <span data-ttu-id="db9ae-118">Остановить</span><span class="sxs-lookup"><span data-stu-id="db9ae-118">Stop</span></span>
- <span data-ttu-id="db9ae-119">Рвать</span><span class="sxs-lookup"><span data-stu-id="db9ae-119">Suspend</span></span>

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

### <span data-ttu-id="db9ae-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="db9ae-120">-InformationVariable</span></span>
<span data-ttu-id="db9ae-121">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="db9ae-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="db9ae-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="db9ae-122">-Profile</span></span>
<span data-ttu-id="db9ae-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="db9ae-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="db9ae-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="db9ae-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="db9ae-125">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="db9ae-125">-Role</span></span>
<span data-ttu-id="db9ae-126">Указывает массив ролей.</span><span class="sxs-lookup"><span data-stu-id="db9ae-126">Specifies an array of roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9ae-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="db9ae-127">-ServiceName</span></span>
<span data-ttu-id="db9ae-128">Указывает имя службы Azure для развертывания.</span><span class="sxs-lookup"><span data-stu-id="db9ae-128">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="db9ae-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="db9ae-129">-Slot</span></span>
<span data-ttu-id="db9ae-130">Задает среду развертывания, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="db9ae-130">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="db9ae-131">Допустимые значения этого параметра: "производственный" или "промежуточный".</span><span class="sxs-lookup"><span data-stu-id="db9ae-131">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="db9ae-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db9ae-132">CommonParameters</span></span>
<span data-ttu-id="db9ae-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db9ae-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db9ae-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db9ae-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db9ae-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db9ae-135">INPUTS</span></span>

## <span data-ttu-id="db9ae-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db9ae-136">OUTPUTS</span></span>

## <span data-ttu-id="db9ae-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="db9ae-137">NOTES</span></span>

## <span data-ttu-id="db9ae-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db9ae-138">RELATED LINKS</span></span>

[<span data-ttu-id="db9ae-139">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="db9ae-139">Remove-AzureServiceDiagnosticsExtension</span></span>](./Remove-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="db9ae-140">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="db9ae-140">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


