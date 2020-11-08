---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95298AFC-B492-4EA6-AFC2-E862D3086AF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84b1256d7d911d22a4f1344bdf841943ce87ee7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076116"
---
# <span data-ttu-id="dd6b2-101">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="dd6b2-101">Remove-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="dd6b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd6b2-102">SYNOPSIS</span></span>
<span data-ttu-id="dd6b2-103">Удаляет расширение диагностики облачных служб, примененное для всех ролей или именованных ролей в определенном слоте развертывания.</span><span class="sxs-lookup"><span data-stu-id="dd6b2-103">Removes the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="dd6b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd6b2-104">SYNTAX</span></span>

### <span data-ttu-id="dd6b2-105">RemoveByRoles (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dd6b2-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd6b2-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="dd6b2-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [-UninstallConfiguration]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd6b2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd6b2-107">DESCRIPTION</span></span>
<span data-ttu-id="dd6b2-108">Командлет **Remove-AzureServiceDiagnosticsExtension** удаляет расширение диагностики облачных служб, примененное для всех ролей или именованных ролей в определенном слоте развертывания.</span><span class="sxs-lookup"><span data-stu-id="dd6b2-108">The **Remove-AzureServiceDiagnosticsExtension** cmdlet removes the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="dd6b2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd6b2-109">EXAMPLES</span></span>

### <span data-ttu-id="dd6b2-110">Пример 1: удаление расширения диагностики для службы</span><span class="sxs-lookup"><span data-stu-id="dd6b2-110">Example 1: Remove the diagnostic extension for a service</span></span>
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc
```

<span data-ttu-id="dd6b2-111">Эта команда удаляет расширение диагностики для указанной роли.</span><span class="sxs-lookup"><span data-stu-id="dd6b2-111">This command removes the diagnostic extension for a specified role.</span></span>

### <span data-ttu-id="dd6b2-112">Пример 2: удаление расширения диагностики для службы в указанной роли</span><span class="sxs-lookup"><span data-stu-id="dd6b2-112">Example 2: Remove the diagnostic extension for a service in a specified role</span></span>
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc -Role "WebRole01"
```

<span data-ttu-id="dd6b2-113">Эта команда удаляет расширение диагностики для указанной роли.</span><span class="sxs-lookup"><span data-stu-id="dd6b2-113">This command removes the diagnostic extension for a specified role.</span></span>

## <span data-ttu-id="dd6b2-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd6b2-114">PARAMETERS</span></span>

### <span data-ttu-id="dd6b2-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="dd6b2-115">-InformationAction</span></span>
<span data-ttu-id="dd6b2-116">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="dd6b2-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="dd6b2-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="dd6b2-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dd6b2-118">Продолжал</span><span class="sxs-lookup"><span data-stu-id="dd6b2-118">Continue</span></span>
- <span data-ttu-id="dd6b2-119">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="dd6b2-119">Ignore</span></span>
- <span data-ttu-id="dd6b2-120">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="dd6b2-120">Inquire</span></span>
- <span data-ttu-id="dd6b2-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dd6b2-121">SilentlyContinue</span></span>
- <span data-ttu-id="dd6b2-122">Остановить</span><span class="sxs-lookup"><span data-stu-id="dd6b2-122">Stop</span></span>
- <span data-ttu-id="dd6b2-123">Рвать</span><span class="sxs-lookup"><span data-stu-id="dd6b2-123">Suspend</span></span>

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

### <span data-ttu-id="dd6b2-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dd6b2-124">-InformationVariable</span></span>
<span data-ttu-id="dd6b2-125">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="dd6b2-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="dd6b2-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="dd6b2-126">-Profile</span></span>
<span data-ttu-id="dd6b2-127">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="dd6b2-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dd6b2-128">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dd6b2-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dd6b2-129">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="dd6b2-129">-Role</span></span>
<span data-ttu-id="dd6b2-130">Задает необязательный массив ролей, для которого нужно задать конфигурацию удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="dd6b2-130">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="dd6b2-131">Если этот параметр не указан, Конфигурация удаленных рабочих столов будет использоваться по умолчанию для всех ролей.</span><span class="sxs-lookup"><span data-stu-id="dd6b2-131">If you do not specify this parameter, the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="dd6b2-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="dd6b2-132">-ServiceName</span></span>
<span data-ttu-id="dd6b2-133">Указывает имя службы Azure для развертывания.</span><span class="sxs-lookup"><span data-stu-id="dd6b2-133">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="dd6b2-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="dd6b2-134">-Slot</span></span>
<span data-ttu-id="dd6b2-135">Задает среду развертывания, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="dd6b2-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="dd6b2-136">Допустимые значения: Production или промежуточный.</span><span class="sxs-lookup"><span data-stu-id="dd6b2-136">Valid values are Production or Staging.</span></span>

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

### <span data-ttu-id="dd6b2-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd6b2-137">-UninstallConfiguration</span></span>
<span data-ttu-id="dd6b2-138">Указывает, что этот командлет удаляет все конфигурации RDP из облачной службы.</span><span class="sxs-lookup"><span data-stu-id="dd6b2-138">Indicates that this cmdlet uninstalls all RDP configurations from the cloud service.</span></span>

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

### <span data-ttu-id="dd6b2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd6b2-139">CommonParameters</span></span>
<span data-ttu-id="dd6b2-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd6b2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd6b2-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd6b2-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd6b2-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd6b2-142">INPUTS</span></span>

## <span data-ttu-id="dd6b2-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd6b2-143">OUTPUTS</span></span>

## <span data-ttu-id="dd6b2-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd6b2-144">NOTES</span></span>

## <span data-ttu-id="dd6b2-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd6b2-145">RELATED LINKS</span></span>

[<span data-ttu-id="dd6b2-146">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="dd6b2-146">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="dd6b2-147">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="dd6b2-147">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


