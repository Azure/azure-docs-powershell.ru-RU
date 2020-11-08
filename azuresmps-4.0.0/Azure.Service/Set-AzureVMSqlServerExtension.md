---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 56C7B6F5-C2AC-4C5A-8930-645374694CC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 053bb1bfb31b90a91d69e50b77ac6411321014f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075790"
---
# <span data-ttu-id="a3a29-101">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="a3a29-101">Set-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="a3a29-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a3a29-102">SYNOPSIS</span></span>
<span data-ttu-id="a3a29-103">Задает расширение Azure SQL Server на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a3a29-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="a3a29-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a3a29-104">SYNTAX</span></span>

### <span data-ttu-id="a3a29-105">EnableSqlServerExtension (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a3a29-105">EnableSqlServerExtension (Default)</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>]
 [[-AutoPatchingSettings] <AutoPatchingSettings>] [[-AutoBackupSettings] <AutoBackupSettings>]
 [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a3a29-106">DisableSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="a3a29-106">DisableSqlServerExtension</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Disable] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3a29-107">UninstallSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="a3a29-107">UninstallSqlServerExtension</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Uninstall]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a3a29-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3a29-108">DESCRIPTION</span></span>
<span data-ttu-id="a3a29-109">Командлет **Set-AzureVMSqlServerExtension** задает расширение Azure SQL Server на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a3a29-109">The **Set-AzureVMSqlServerExtension** cmdlet sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="a3a29-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a3a29-110">EXAMPLES</span></span>

### <span data-ttu-id="a3a29-111">Пример 1: Настройка параметров автоматического исправления на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="a3a29-111">Example 1: Set auto-patching settings on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ServiceName" -Name "VMName" | Set-AzureVMSqlServerExtension -AutoPatchingSettings $APS | Update-AzureVM
```

<span data-ttu-id="a3a29-112">Эта команда задает параметры автоматического исправления для виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="a3a29-112">This command sets auto-patching settings on an Azure virtual machine.</span></span>

### <span data-ttu-id="a3a29-113">Пример 2: Настройка параметров автоматического резервного копирования на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="a3a29-113">Example 2: Set auto-backup settings on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ServiceName" -Name "VMName" | Set-AzureVMSqlServerExtension -AutoBackupSettings $ABS | Update-AzureVM
```

<span data-ttu-id="a3a29-114">Эта команда задает параметры автоматического резервного копирования на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="a3a29-114">This command sets auto-backup settings on Azure virtual machine.</span></span>

### <span data-ttu-id="a3a29-115">Пример 3: отключение расширения SQL Server на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="a3a29-115">Example 3: Disable an SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Set-AzureVMSqlServerExtension -Disable
```

<span data-ttu-id="a3a29-116">Эта команда отключает расширение виртуальной машины SQL Server на данной виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a3a29-116">This command disables SQL Server virtual machine extension on a given virtual machine.</span></span>

### <span data-ttu-id="a3a29-117">Пример 4: удаление расширения SQL Server на определенной виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="a3a29-117">Example 4: Uninstall an SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Set-AzureVMSqlServerExtension -Uninstall
```

<span data-ttu-id="a3a29-118">Эта команда удаляет расширение виртуальной машины SQL Server на виртуальной машине с именем VMName.</span><span class="sxs-lookup"><span data-stu-id="a3a29-118">This command uninstalls a SQL Server virtual machine extension on the virtual machine named VMName.</span></span>

## <span data-ttu-id="a3a29-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a3a29-119">PARAMETERS</span></span>

### <span data-ttu-id="a3a29-120">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="a3a29-120">-AutoBackupSettings</span></span>
<span data-ttu-id="a3a29-121">Задает параметры автоматического резервного копирования SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a3a29-121">Specifies the automatic SQL Server backup settings.</span></span>

```yaml
Type: AutoBackupSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3a29-122">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="a3a29-122">-AutoPatchingSettings</span></span>
<span data-ttu-id="a3a29-123">Задает параметры автоматического исправления SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a3a29-123">Specifies the automatic SQL Server patching settings.</span></span>

```yaml
Type: AutoPatchingSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3a29-124">-Отключение</span><span class="sxs-lookup"><span data-stu-id="a3a29-124">-Disable</span></span>
<span data-ttu-id="a3a29-125">Указывает на то, что этот командлет отключает состояние расширения.</span><span class="sxs-lookup"><span data-stu-id="a3a29-125">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableSqlServerExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3a29-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a3a29-126">-InformationAction</span></span>
<span data-ttu-id="a3a29-127">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="a3a29-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a3a29-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a3a29-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a3a29-129">Продолжал</span><span class="sxs-lookup"><span data-stu-id="a3a29-129">Continue</span></span>
- <span data-ttu-id="a3a29-130">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="a3a29-130">Ignore</span></span>
- <span data-ttu-id="a3a29-131">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="a3a29-131">Inquire</span></span>
- <span data-ttu-id="a3a29-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a3a29-132">SilentlyContinue</span></span>
- <span data-ttu-id="a3a29-133">Остановить</span><span class="sxs-lookup"><span data-stu-id="a3a29-133">Stop</span></span>
- <span data-ttu-id="a3a29-134">Рвать</span><span class="sxs-lookup"><span data-stu-id="a3a29-134">Suspend</span></span>

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

### <span data-ttu-id="a3a29-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a3a29-135">-InformationVariable</span></span>
<span data-ttu-id="a3a29-136">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="a3a29-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a3a29-137">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="a3a29-137">-KeyVaultCredentialSettings</span></span>
<span data-ttu-id="a3a29-138">Задает параметры учетных данных для ключевого хранилища.</span><span class="sxs-lookup"><span data-stu-id="a3a29-138">Specifies key vault credential settings.</span></span>

```yaml
Type: KeyVaultCredentialSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3a29-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="a3a29-139">-Profile</span></span>
<span data-ttu-id="a3a29-140">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a3a29-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a3a29-141">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a3a29-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a3a29-142">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="a3a29-142">-ReferenceName</span></span>
<span data-ttu-id="a3a29-143">Указывает имя ссылки на расширение SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a3a29-143">Specifies the reference name of the SQL Server extension.</span></span>

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

### <span data-ttu-id="a3a29-144">-Удаление</span><span class="sxs-lookup"><span data-stu-id="a3a29-144">-Uninstall</span></span>
<span data-ttu-id="a3a29-145">Указывает, что этот командлет удаляет расширение SQL Server с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a3a29-145">Indicates that this cmdlet uninstalls the SQL Server extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallSqlServerExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3a29-146">-Version</span><span class="sxs-lookup"><span data-stu-id="a3a29-146">-Version</span></span>
<span data-ttu-id="a3a29-147">Указывает версию расширения SQL Server, из которой Get-AzureVMSqlServerExtension извлекает параметры.</span><span class="sxs-lookup"><span data-stu-id="a3a29-147">Specifies the version of the SQL Server extension that Get-AzureVMSqlServerExtension retrieves settings from.</span></span>

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

### <span data-ttu-id="a3a29-148">-VM</span><span class="sxs-lookup"><span data-stu-id="a3a29-148">-VM</span></span>
<span data-ttu-id="a3a29-149">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a3a29-149">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3a29-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3a29-150">CommonParameters</span></span>
<span data-ttu-id="a3a29-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a3a29-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3a29-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3a29-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3a29-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a3a29-153">INPUTS</span></span>

## <span data-ttu-id="a3a29-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3a29-154">OUTPUTS</span></span>

## <span data-ttu-id="a3a29-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="a3a29-155">NOTES</span></span>

## <span data-ttu-id="a3a29-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3a29-156">RELATED LINKS</span></span>

[<span data-ttu-id="a3a29-157">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="a3a29-157">Get-AzureVMSqlServerExtension</span></span>](./Get-AzureVMSqlServerExtension.md)

[<span data-ttu-id="a3a29-158">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="a3a29-158">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)


