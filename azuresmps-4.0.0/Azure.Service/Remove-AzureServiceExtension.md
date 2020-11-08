---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6B5E4968-5DF5-4956-A070-9F54A79D960B
online version: ''
schema: 2.0.0
ms.openlocfilehash: f45e0a93b2f6261ca6031aa721bda3a72f4443dd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076113"
---
# <span data-ttu-id="3570c-101">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="3570c-101">Remove-AzureServiceExtension</span></span>

## <span data-ttu-id="3570c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3570c-102">SYNOPSIS</span></span>
<span data-ttu-id="3570c-103">Удаление расширений облачной службы, применяемых к развертыванию.</span><span class="sxs-lookup"><span data-stu-id="3570c-103">Removes cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="3570c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3570c-104">SYNTAX</span></span>

### <span data-ttu-id="3570c-105">RemoveByRoles (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3570c-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-ExtensionName] <String> [-ProviderNamespace] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3570c-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="3570c-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-UninstallConfiguration] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3570c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3570c-107">DESCRIPTION</span></span>
<span data-ttu-id="3570c-108">Командлет **Remove-AzureServiceExtension** удаляет расширения облачной службы, применяемые к развертыванию.</span><span class="sxs-lookup"><span data-stu-id="3570c-108">The **Remove-AzureServiceExtension** cmdlet removes cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="3570c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3570c-109">EXAMPLES</span></span>

### <span data-ttu-id="3570c-110">Пример 1: удаление расширения службы</span><span class="sxs-lookup"><span data-stu-id="3570c-110">Example 1: Remove a service extension</span></span>
```
PS C:\> Remove-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions"
```

<span data-ttu-id="3570c-111">Эта команда удаляет расширение службы.</span><span class="sxs-lookup"><span data-stu-id="3570c-111">This command removes a service extension.</span></span>

### <span data-ttu-id="3570c-112">Пример 2: удаление расширения службы и удаление всех конфигураций</span><span class="sxs-lookup"><span data-stu-id="3570c-112">Example 2: Remove a service extension and uninstall all configurations</span></span>
```
PS C:\> Remove-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -UninstallConfiguration
```

<span data-ttu-id="3570c-113">Эта команда удаляет расширение службы и удалит все конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3570c-113">This command removes a service extension and uninstalls all configurations.</span></span>

## <span data-ttu-id="3570c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3570c-114">PARAMETERS</span></span>

### <span data-ttu-id="3570c-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="3570c-115">-ExtensionName</span></span>
<span data-ttu-id="3570c-116">Задает имя расширения.</span><span class="sxs-lookup"><span data-stu-id="3570c-116">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3570c-117">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3570c-117">-InformationAction</span></span>
<span data-ttu-id="3570c-118">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="3570c-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3570c-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3570c-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3570c-120">Продолжал</span><span class="sxs-lookup"><span data-stu-id="3570c-120">Continue</span></span>
- <span data-ttu-id="3570c-121">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="3570c-121">Ignore</span></span>
- <span data-ttu-id="3570c-122">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="3570c-122">Inquire</span></span>
- <span data-ttu-id="3570c-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3570c-123">SilentlyContinue</span></span>
- <span data-ttu-id="3570c-124">Остановить</span><span class="sxs-lookup"><span data-stu-id="3570c-124">Stop</span></span>
- <span data-ttu-id="3570c-125">Рвать</span><span class="sxs-lookup"><span data-stu-id="3570c-125">Suspend</span></span>

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

### <span data-ttu-id="3570c-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3570c-126">-InformationVariable</span></span>
<span data-ttu-id="3570c-127">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="3570c-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3570c-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="3570c-128">-Profile</span></span>
<span data-ttu-id="3570c-129">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3570c-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3570c-130">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3570c-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3570c-131">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="3570c-131">-ProviderNamespace</span></span>
<span data-ttu-id="3570c-132">Задает пространство имен поставщика расширений.</span><span class="sxs-lookup"><span data-stu-id="3570c-132">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3570c-133">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="3570c-133">-Role</span></span>
<span data-ttu-id="3570c-134">Задает необязательный массив ролей, для которого нужно указать расширение.</span><span class="sxs-lookup"><span data-stu-id="3570c-134">Specifies an optional array of roles to specify the extension for.</span></span>
<span data-ttu-id="3570c-135">Если не указано, расширение применяется как конфигурация по умолчанию для всех ролей.</span><span class="sxs-lookup"><span data-stu-id="3570c-135">If not specified the extension is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: RemoveByRoles
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3570c-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3570c-136">-ServiceName</span></span>
<span data-ttu-id="3570c-137">Указывает имя облачной службы.</span><span class="sxs-lookup"><span data-stu-id="3570c-137">Specifies the cloud service name.</span></span>

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

### <span data-ttu-id="3570c-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="3570c-138">-Slot</span></span>
<span data-ttu-id="3570c-139">Задает среду развертывания, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="3570c-139">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="3570c-140">Допустимые значения: Production или промежуточный.</span><span class="sxs-lookup"><span data-stu-id="3570c-140">Valid values are Production or Staging.</span></span>

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

### <span data-ttu-id="3570c-141">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="3570c-141">-UninstallConfiguration</span></span>
<span data-ttu-id="3570c-142">Указывает, что этот командлет удаляет все конфигурации из облачной службы.</span><span class="sxs-lookup"><span data-stu-id="3570c-142">Indicates that this cmdlet uninstalls all configurations from the cloud service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAllRoles
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3570c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3570c-143">CommonParameters</span></span>
<span data-ttu-id="3570c-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3570c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3570c-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3570c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3570c-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3570c-146">INPUTS</span></span>

## <span data-ttu-id="3570c-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3570c-147">OUTPUTS</span></span>

## <span data-ttu-id="3570c-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="3570c-148">NOTES</span></span>

## <span data-ttu-id="3570c-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3570c-149">RELATED LINKS</span></span>

[<span data-ttu-id="3570c-150">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="3570c-150">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="3570c-151">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="3570c-151">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


