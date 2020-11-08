---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C263CCAD-E51F-420E-9AD4-4FAC09C99CB1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3c10a7694034fe4400ed415891e74f7089ce8558
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076112"
---
# <span data-ttu-id="4f1fd-101">Remove-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="4f1fd-101">Remove-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="4f1fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4f1fd-102">SYNOPSIS</span></span>
<span data-ttu-id="4f1fd-103">Удаляет расширение удаленного рабочего стола облачной службы, примененное ко всем ролям или именованным ролям в указанном слоте развертывания.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-103">Removes the cloud service remote desktop extension applied on all roles or named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="4f1fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4f1fd-104">SYNTAX</span></span>

### <span data-ttu-id="4f1fd-105">RemoveByRoles (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4f1fd-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f1fd-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="4f1fd-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>]
 [-UninstallConfiguration] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4f1fd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f1fd-107">DESCRIPTION</span></span>
<span data-ttu-id="4f1fd-108">Командлет **Remove-AzureServiceRemoteDesktopExtension** удаляет расширение удаленного рабочего стола облачной службы, примененное ко всем ролям или именованным ролям в определенном слоте развертывания.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-108">The **Remove-AzureServiceRemoteDesktopExtension** cmdlet removes the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="4f1fd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4f1fd-109">EXAMPLES</span></span>

### <span data-ttu-id="4f1fd-110">Пример 1: удаление расширения удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="4f1fd-110">Example 1: Remove the remote desktop extension</span></span>
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc
```

<span data-ttu-id="4f1fd-111">Эта команда удаляет расширение удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-111">This command removes the remote desktop extension.</span></span>

### <span data-ttu-id="4f1fd-112">Пример 2: удаление расширения удаленных рабочих столов для указанной роли</span><span class="sxs-lookup"><span data-stu-id="4f1fd-112">Example 2: Remove the remote desktop extension from a specified role</span></span>
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc -Role "WebRole1"
```

<span data-ttu-id="4f1fd-113">Эта команда удаляет расширение "удаленный рабочий стол" для указанной роли.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-113">This command removes the remote desktop extension from a specified role.</span></span>

## <span data-ttu-id="4f1fd-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4f1fd-114">PARAMETERS</span></span>

### <span data-ttu-id="4f1fd-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4f1fd-115">-InformationAction</span></span>
<span data-ttu-id="4f1fd-116">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4f1fd-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4f1fd-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4f1fd-118">Продолжал</span><span class="sxs-lookup"><span data-stu-id="4f1fd-118">Continue</span></span>
- <span data-ttu-id="4f1fd-119">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="4f1fd-119">Ignore</span></span>
- <span data-ttu-id="4f1fd-120">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="4f1fd-120">Inquire</span></span>
- <span data-ttu-id="4f1fd-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4f1fd-121">SilentlyContinue</span></span>
- <span data-ttu-id="4f1fd-122">Остановить</span><span class="sxs-lookup"><span data-stu-id="4f1fd-122">Stop</span></span>
- <span data-ttu-id="4f1fd-123">Рвать</span><span class="sxs-lookup"><span data-stu-id="4f1fd-123">Suspend</span></span>

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

### <span data-ttu-id="4f1fd-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4f1fd-124">-InformationVariable</span></span>
<span data-ttu-id="4f1fd-125">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4f1fd-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="4f1fd-126">-Profile</span></span>
<span data-ttu-id="4f1fd-127">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4f1fd-128">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4f1fd-129">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="4f1fd-129">-Role</span></span>
<span data-ttu-id="4f1fd-130">Задает необязательный массив ролей, для которого нужно указать конфигурацию удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-130">Specifies an optional array of roles to specify the remote desktop configuration for.</span></span>
<span data-ttu-id="4f1fd-131">Если не указана конфигурация удаленных рабочих столов, она будет использоваться по умолчанию для всех ролей.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-131">If not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="4f1fd-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4f1fd-132">-ServiceName</span></span>
<span data-ttu-id="4f1fd-133">Указывает имя службы Azure для развертывания.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-133">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="4f1fd-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="4f1fd-134">-Slot</span></span>
<span data-ttu-id="4f1fd-135">Задает среду развертывания, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="4f1fd-136">Поддерживаются значения "производство" или "промежуточное хранение".</span><span class="sxs-lookup"><span data-stu-id="4f1fd-136">Supported values are "Production" or "Staging".</span></span>

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

### <span data-ttu-id="4f1fd-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f1fd-137">-UninstallConfiguration</span></span>
<span data-ttu-id="4f1fd-138">Указывает, что этот командлет удаляет все конфигурации RDP из облачной службы.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-138">Specifies that this cmdlet uninstalls all RDP configurations from the cloud service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAllRoles
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f1fd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f1fd-139">CommonParameters</span></span>
<span data-ttu-id="4f1fd-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f1fd-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f1fd-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f1fd-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4f1fd-142">INPUTS</span></span>

## <span data-ttu-id="4f1fd-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f1fd-143">OUTPUTS</span></span>

## <span data-ttu-id="4f1fd-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="4f1fd-144">NOTES</span></span>

## <span data-ttu-id="4f1fd-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f1fd-145">RELATED LINKS</span></span>

[<span data-ttu-id="4f1fd-146">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="4f1fd-146">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


