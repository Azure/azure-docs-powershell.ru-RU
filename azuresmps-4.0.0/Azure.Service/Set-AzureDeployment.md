---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7F51F534-6C64-4983-A08F-4732A39C2E7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c62f3d29b4cd2c87fd5606ca013eb03958fb62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076064"
---
# <span data-ttu-id="44ea1-101">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="44ea1-101">Set-AzureDeployment</span></span>

## <span data-ttu-id="44ea1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44ea1-102">SYNOPSIS</span></span>
<span data-ttu-id="44ea1-103">Изменяет состояние, параметры конфигурации или режим обновления развертывания.</span><span class="sxs-lookup"><span data-stu-id="44ea1-103">Modifies the status, configuration settings, or upgrade mode of a deployment.</span></span>

## <span data-ttu-id="44ea1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44ea1-104">SYNTAX</span></span>

### <span data-ttu-id="44ea1-105">Обновление</span><span class="sxs-lookup"><span data-stu-id="44ea1-105">Upgrade</span></span>
```
Set-AzureDeployment [-Upgrade] [-ServiceName] <String> [-Package] <String> [-Configuration] <String>
 [-Slot] <String> [[-Mode] <String>] [[-Label] <String>] [[-RoleName] <String>] [-Force]
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="44ea1-106">Служба</span><span class="sxs-lookup"><span data-stu-id="44ea1-106">Config</span></span>
```
Set-AzureDeployment [-Config] [-ServiceName] <String> [-Configuration] <String> [-Slot] <String>
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="44ea1-107">Состояни</span><span class="sxs-lookup"><span data-stu-id="44ea1-107">Status</span></span>
```
Set-AzureDeployment [-Status] [-ServiceName] <String> [-Slot] <String> [-NewStatus] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="44ea1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44ea1-108">DESCRIPTION</span></span>
<span data-ttu-id="44ea1-109">Командлет **Set-AzureDeployment** изменяет состояние, параметры конфигурации или режим обновления для развертывания Azure.</span><span class="sxs-lookup"><span data-stu-id="44ea1-109">The **Set-AzureDeployment** cmdlet modifies the status, configuration settings, or upgrade mode of an Azure deployment.</span></span>
<span data-ttu-id="44ea1-110">Вы можете изменить состояние развертывания на "запущено" или "приостановлено".</span><span class="sxs-lookup"><span data-stu-id="44ea1-110">You can change the status of the deployment to either Running or Suspended.</span></span>
<span data-ttu-id="44ea1-111">Вы можете изменить CSCFG файл для развертывания.</span><span class="sxs-lookup"><span data-stu-id="44ea1-111">You can change the .cscfg file for the deployment.</span></span>
<span data-ttu-id="44ea1-112">Вы можете настроить режим обновления и файлы конфигурации обновления.</span><span class="sxs-lookup"><span data-stu-id="44ea1-112">You can set the upgrade mode and update configuration files.</span></span>
<span data-ttu-id="44ea1-113">Используйте командлет **Set-AzureWalkUpgradeDomain** , чтобы начать обновление.</span><span class="sxs-lookup"><span data-stu-id="44ea1-113">Use the **Set-AzureWalkUpgradeDomain** cmdlet to initiate an upgrade.</span></span>

## <span data-ttu-id="44ea1-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44ea1-114">EXAMPLES</span></span>

### <span data-ttu-id="44ea1-115">Пример 1: изменение состояния развертывания</span><span class="sxs-lookup"><span data-stu-id="44ea1-115">Example 1: Change the status of a deployment</span></span>
```
PS C:\> Set-AzureDeployment -Status -ServiceName "ContosoService" -Slot "Production" -NewStatus "Running"
```

<span data-ttu-id="44ea1-116">Эта команда задает состояние развертывания для службы с именем ContosoService в рабочей среде для выполнения.</span><span class="sxs-lookup"><span data-stu-id="44ea1-116">This command sets the status of the deployment for the service named ContosoService in the production environment to Running.</span></span>

### <span data-ttu-id="44ea1-117">Пример 2: назначение другого файла конфигурации для развертывания</span><span class="sxs-lookup"><span data-stu-id="44ea1-117">Example 2: Assign a different configuration file to a deployment</span></span>
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Slot "Staging" -Configuration "C:\Temp\MyServiceConfig.Cloud.csfg"
```

<span data-ttu-id="44ea1-118">Эта команда назначает другой файл конфигурации для развертывания службы с именем ContosoService в промежуточной среде.</span><span class="sxs-lookup"><span data-stu-id="44ea1-118">This command assigns a different configuration file for the deployment for the service named ContosoService in the staging environment.</span></span>

### <span data-ttu-id="44ea1-119">Пример 3: Настройка режима обновления на авто</span><span class="sxs-lookup"><span data-stu-id="44ea1-119">Example 3: Set the upgrade mode to Auto</span></span>
```
PS C:\> Set-AzureDeployment -Upgrade -ServiceName "ContosoService" -Mode Auto -Package "C:\packages\ContosoApp.cspkg" -Configuration "C:\Config\ContosoServiceConfig.Cloud.csfg"
```

<span data-ttu-id="44ea1-120">Эта команда задает автоматический режим обновления, а также указывает пакет обновления и новый файл конфигурации.</span><span class="sxs-lookup"><span data-stu-id="44ea1-120">This command sets the upgrade mode to Auto, and specifies an upgrade package and a new configuration file.</span></span>

### <span data-ttu-id="44ea1-121">Пример 4: Установка конфигурации расширения в службе</span><span class="sxs-lookup"><span data-stu-id="44ea1-121">Example 4: Install extension configuration in a service</span></span>
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Mode "Automatic" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Slot "Production" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

<span data-ttu-id="44ea1-122">Эта команда устанавливает конфигурацию расширения в указанную облачную службу и применяет их к ролям.</span><span class="sxs-lookup"><span data-stu-id="44ea1-122">This command installs the extension configuration in the specified Cloud Service and applies them on roles.</span></span>

## <span data-ttu-id="44ea1-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44ea1-123">PARAMETERS</span></span>

### <span data-ttu-id="44ea1-124">-Config</span><span class="sxs-lookup"><span data-stu-id="44ea1-124">-Config</span></span>
<span data-ttu-id="44ea1-125">Указывает на то, что этот командлет изменяет конфигурацию развертывания.</span><span class="sxs-lookup"><span data-stu-id="44ea1-125">Specifies that this cmdlet modifies the configuration of the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Config
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ea1-126">-Configuration</span><span class="sxs-lookup"><span data-stu-id="44ea1-126">-Configuration</span></span>
<span data-ttu-id="44ea1-127">Указывает полный путь к CSCFG-файлу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="44ea1-127">Specifies the full path of a .cscfg configuration file.</span></span>
<span data-ttu-id="44ea1-128">Вы можете указать файл конфигурации для обновления или изменения конфигурации.</span><span class="sxs-lookup"><span data-stu-id="44ea1-128">You can specify a configuration file for an upgrade or configuration change.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade, Config
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ea1-129">-ExtensionConfiguration</span><span class="sxs-lookup"><span data-stu-id="44ea1-129">-ExtensionConfiguration</span></span>
<span data-ttu-id="44ea1-130">Задает массив объектов конфигурации расширения.</span><span class="sxs-lookup"><span data-stu-id="44ea1-130">Specifies an array of extension configuration objects.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: Upgrade, Config
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44ea1-131">-Force</span><span class="sxs-lookup"><span data-stu-id="44ea1-131">-Force</span></span>
<span data-ttu-id="44ea1-132">Указывает на то, что командлет выполняет принудительное обновление.</span><span class="sxs-lookup"><span data-stu-id="44ea1-132">Indicates that cmdlet performs a forced upgrade.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ea1-133">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="44ea1-133">-InformationAction</span></span>
<span data-ttu-id="44ea1-134">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="44ea1-134">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="44ea1-135">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="44ea1-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="44ea1-136">Продолжал</span><span class="sxs-lookup"><span data-stu-id="44ea1-136">Continue</span></span>
- <span data-ttu-id="44ea1-137">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="44ea1-137">Ignore</span></span>
- <span data-ttu-id="44ea1-138">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="44ea1-138">Inquire</span></span>
- <span data-ttu-id="44ea1-139">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="44ea1-139">SilentlyContinue</span></span>
- <span data-ttu-id="44ea1-140">Остановить</span><span class="sxs-lookup"><span data-stu-id="44ea1-140">Stop</span></span>
- <span data-ttu-id="44ea1-141">Рвать</span><span class="sxs-lookup"><span data-stu-id="44ea1-141">Suspend</span></span>

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

### <span data-ttu-id="44ea1-142">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="44ea1-142">-InformationVariable</span></span>
<span data-ttu-id="44ea1-143">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="44ea1-143">Specifies an information variable.</span></span>

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

### <span data-ttu-id="44ea1-144">-Label</span><span class="sxs-lookup"><span data-stu-id="44ea1-144">-Label</span></span>
<span data-ttu-id="44ea1-145">Указывает метку для обновленного развертывания.</span><span class="sxs-lookup"><span data-stu-id="44ea1-145">Specifies a label for the upgraded deployment.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ea1-146">Режим</span><span class="sxs-lookup"><span data-stu-id="44ea1-146">-Mode</span></span>
<span data-ttu-id="44ea1-147">Задает режим обновления.</span><span class="sxs-lookup"><span data-stu-id="44ea1-147">Specifies the mode of upgrade.</span></span>
<span data-ttu-id="44ea1-148">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="44ea1-148">Valid values are:</span></span> 

- <span data-ttu-id="44ea1-149">Авто</span><span class="sxs-lookup"><span data-stu-id="44ea1-149">Auto</span></span> 
- <span data-ttu-id="44ea1-150">Вручную</span><span class="sxs-lookup"><span data-stu-id="44ea1-150">Manual</span></span> 
- <span data-ttu-id="44ea1-151">Подключен</span><span class="sxs-lookup"><span data-stu-id="44ea1-151">Simultaneous</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ea1-152">-NewStatus</span><span class="sxs-lookup"><span data-stu-id="44ea1-152">-NewStatus</span></span>
<span data-ttu-id="44ea1-153">Указывает целевое состояние для развертывания.</span><span class="sxs-lookup"><span data-stu-id="44ea1-153">Specifies the target status for the deployment.</span></span>
<span data-ttu-id="44ea1-154">Допустимые значения: запущено и приостановлено.</span><span class="sxs-lookup"><span data-stu-id="44ea1-154">Valid values are: Running and Suspended.</span></span>

```yaml
Type: String
Parameter Sets: Status
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ea1-155">-Package</span><span class="sxs-lookup"><span data-stu-id="44ea1-155">-Package</span></span>
<span data-ttu-id="44ea1-156">Указывает полный путь к файлу пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="44ea1-156">Specifies the full path of an upgrade package file.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ea1-157">-Profile</span><span class="sxs-lookup"><span data-stu-id="44ea1-157">-Profile</span></span>
<span data-ttu-id="44ea1-158">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="44ea1-158">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="44ea1-159">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="44ea1-159">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="44ea1-160">-RoleName</span><span class="sxs-lookup"><span data-stu-id="44ea1-160">-RoleName</span></span>
<span data-ttu-id="44ea1-161">Указывает имя роли для обновления.</span><span class="sxs-lookup"><span data-stu-id="44ea1-161">Specifies the name of the role to upgrade.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ea1-162">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="44ea1-162">-ServiceName</span></span>
<span data-ttu-id="44ea1-163">Указывает имя службы Azure для развертывания.</span><span class="sxs-lookup"><span data-stu-id="44ea1-163">Specifies the name of the Azure service of the deployment.</span></span>

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

### <span data-ttu-id="44ea1-164">-Slot</span><span class="sxs-lookup"><span data-stu-id="44ea1-164">-Slot</span></span>
<span data-ttu-id="44ea1-165">Задает среду развертывания, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="44ea1-165">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="44ea1-166">Допустимые значения: "производство" и "промежуточный".</span><span class="sxs-lookup"><span data-stu-id="44ea1-166">Valid values are: Production and Staging.</span></span>

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

### <span data-ttu-id="44ea1-167">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="44ea1-167">-Status</span></span>
<span data-ttu-id="44ea1-168">Указывает, что этот командлет изменяет состояние развертывания.</span><span class="sxs-lookup"><span data-stu-id="44ea1-168">Specifies that this cmdlet changes the status of the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Status
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ea1-169">-Обновление</span><span class="sxs-lookup"><span data-stu-id="44ea1-169">-Upgrade</span></span>
<span data-ttu-id="44ea1-170">Указывает, что этот командлет обновляет развертывание.</span><span class="sxs-lookup"><span data-stu-id="44ea1-170">Specifies that this cmdlet upgrades the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ea1-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44ea1-171">CommonParameters</span></span>
<span data-ttu-id="44ea1-172">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44ea1-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44ea1-173">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44ea1-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44ea1-174">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44ea1-174">INPUTS</span></span>

## <span data-ttu-id="44ea1-175">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44ea1-175">OUTPUTS</span></span>

## <span data-ttu-id="44ea1-176">Пуск</span><span class="sxs-lookup"><span data-stu-id="44ea1-176">NOTES</span></span>

## <span data-ttu-id="44ea1-177">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44ea1-177">RELATED LINKS</span></span>

[<span data-ttu-id="44ea1-178">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="44ea1-178">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="44ea1-179">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="44ea1-179">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="44ea1-180">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="44ea1-180">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="44ea1-181">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="44ea1-181">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="44ea1-182">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="44ea1-182">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="44ea1-183">Set-AzureWalkUpgradeDomain</span><span class="sxs-lookup"><span data-stu-id="44ea1-183">Set-AzureWalkUpgradeDomain</span></span>](./Set-AzureWalkUpgradeDomain.md)


