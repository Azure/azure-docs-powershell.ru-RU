---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CE1C6576-234E-4891-9158-FA45B64B786C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41e8641b01dcb95a6b6939ff3551fe03b642ddf0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075435"
---
# <span data-ttu-id="26e41-101">Set-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="26e41-101">Set-AzureStorSimpleVirtualDevice</span></span>

## <span data-ttu-id="26e41-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="26e41-102">SYNOPSIS</span></span>
<span data-ttu-id="26e41-103">Создание или обновление конфигурации устройства виртуального устройства StorSimple.</span><span class="sxs-lookup"><span data-stu-id="26e41-103">Creates or updates the device configuration of a StorSimple virtual device.</span></span>

## <span data-ttu-id="26e41-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="26e41-104">SYNTAX</span></span>

```
Set-AzureStorSimpleVirtualDevice -DeviceName <String> -SecretKey <String> -AdministratorPassword <String>
 -SnapshotManagerPassword <String> [-TimeZone <TimeZoneInfo>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="26e41-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26e41-105">DESCRIPTION</span></span>
<span data-ttu-id="26e41-106">Командлет **Set-AzureStorSimpleVirtualDevice** создает или обновляет конфигурацию устройства виртуального устройства Azure StorSimple.</span><span class="sxs-lookup"><span data-stu-id="26e41-106">The **Set-AzureStorSimpleVirtualDevice** cmdlet creates or updates the device configuration of an Azure StorSimple virtual device.</span></span>

## <span data-ttu-id="26e41-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="26e41-107">EXAMPLES</span></span>

### <span data-ttu-id="26e41-108">Пример 1: Обновление виртуального устройства</span><span class="sxs-lookup"><span data-stu-id="26e41-108">Example 1: Update a virtual device</span></span>
```
PS C:\>$TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> Set-AzureStorSimpleVirtualDevice -DeviceName "Contoso23" -SecretKey "wcZBlBGpCMf4USdSKyt/SQ==" -TimeZone $TimeZoneInfo
VERBOSE: ClientRequestId: e31f0d6b-451d-4c1d-b2f1-3fc84c13972c_PS
VERBOSE: ClientRequestId: df58db83-d563-4a2e-bbb4-9576f0e69ca6_PS
VERBOSE: ClientRequestId: 494a9f0d-79ee-4fde-ab4d-85ee5a357556_PS
VERBOSE: ClientRequestId: ce557cbf-174d-4301-93d4-5ffe082c8413_PS
VERBOSE: ClientRequestId: 31284dad-de2c-4758-a2ef-45962875bfa6_PS
VERBOSE: About to configure the device : win-ff93i74m1e1 ! 
VERBOSE: ClientRequestId: d9c66302-45d8-488a-adda-8ccf957f77d3_PS


TaskId       : 21f530c3-bc47-4591-8c4e-da4d694b751d
TaskResult   : Succeeded
TaskStatus   : Completed
ErrorCode    : 
ErrorMessage : 
TaskSteps    : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: a94f972c-18ea-40b6-9401-2ad209c0c8b4_PS
AlertNotification              : Microsoft.WindowsAzure.Management.StorSimple.Models.AlertNotificationSettings
Chap                           : Microsoft.WindowsAzure.Management.StorSimple.Models.ChapSettings
DeviceProperties               : Microsoft.WindowsAzure.Management.StorSimple.Models.DeviceInfo
DnsServer                      : Microsoft.WindowsAzure.Management.StorSimple.Models.DnsServerSettings
InstanceId                     : d369ebb4-8b9a-47fc-9a6b-60f371e123ae
Name                           : 
NetInterfaceList               : {}
OperationInProgress            : None
RemoteMgmtSettingsInfo         : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteManagementSettings
RemoteMinishellSecretInfo      : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteMinishellSettings
SecretEncryptionCertThumbprint : 
Snapshot                       : Microsoft.WindowsAzure.Management.StorSimple.Models.SnapshotSettings
TimeServer                     : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeSettings
Type                           : VirtualAppliance
VirtualApplianceProperties     : Microsoft.WindowsAzure.Management.StorSimple.Models.VirtualApplianceInfo
WebProxy                       : Microsoft.WindowsAzure.Management.StorSimple.Models.WebProxySettings

VERBOSE: Successfully updated configuration for device Contoso23 with id d369ebb4-8b9a-47fc-9a6b-60f371e123ae
```

<span data-ttu-id="26e41-109">Первая команда использует класс **System. TimeZoneInfo** .NET и стандартный синтаксис для получения стандартного тихоокеанское значение часового пояса и сохраняет этот объект в переменной $TimeZoneInfo.</span><span class="sxs-lookup"><span data-stu-id="26e41-109">The first command uses the **System.TimeZoneInfo** .NET class and standard syntax to get Pacific Standard Time zone, and stores that object in the $TimeZoneInfo variable.</span></span>

<span data-ttu-id="26e41-110">Вторая команда обновляет устройство с именем Contoso23, чтобы использовать часовой пояс, указанный в $TimeZoneInfo.</span><span class="sxs-lookup"><span data-stu-id="26e41-110">The second command updates the device named Contoso23 to use the time zone specified in $TimeZoneInfo.</span></span>
<span data-ttu-id="26e41-111">Для использования команды требуется секретный ключ для доступа к конфигурации виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="26e41-111">The command requires the secret key to access the virtual device configuration.</span></span>

### <span data-ttu-id="26e41-112">Пример 2: Обновление виртуального устройства с помощью оператора Pipeline</span><span class="sxs-lookup"><span data-stu-id="26e41-112">Example 2: Update a virtual device by using the pipeline operator</span></span>
```
PS C:\> [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" } | Set-AzureStorSimpleVirtualDevice -DeviceName "Contoso23" -SecretKey "wcZBlBGpCMf4USdSKyt/SQ=="
```

<span data-ttu-id="26e41-113">Эта команда обновляет устройство с именем Contoso23, чтобы использовать часовой пояс, создаваемый командой.</span><span class="sxs-lookup"><span data-stu-id="26e41-113">This command updates the device named Contoso23 to use the time zone that the command creates.</span></span>
<span data-ttu-id="26e41-114">Для использования команды требуется секретный ключ для доступа к конфигурации виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="26e41-114">The command requires the secret key to access the virtual device configuration.</span></span>
<span data-ttu-id="26e41-115">Эта команда действует так же, как и в предыдущем примере, за исключением того, что он передает часовой пояс текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="26e41-115">This command works the same way as the previous example, except that it passes the time zone to the current cmdlet by using the pipeline operator.</span></span>

## <span data-ttu-id="26e41-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="26e41-116">PARAMETERS</span></span>

### <span data-ttu-id="26e41-117">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="26e41-117">-AdministratorPassword</span></span>
<span data-ttu-id="26e41-118">Указывает пароль администратора виртуального устройства, которое нужно настроить.</span><span class="sxs-lookup"><span data-stu-id="26e41-118">Specifies the administrator password of the virtual device to configure.</span></span>

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

### <span data-ttu-id="26e41-119">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="26e41-119">-DeviceName</span></span>
<span data-ttu-id="26e41-120">Указывает имя виртуального устройства для настройки.</span><span class="sxs-lookup"><span data-stu-id="26e41-120">Specifies the name of the virtual device to configure.</span></span>

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

### <span data-ttu-id="26e41-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="26e41-121">-Profile</span></span>
<span data-ttu-id="26e41-122">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="26e41-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="26e41-123">-SecretKey</span><span class="sxs-lookup"><span data-stu-id="26e41-123">-SecretKey</span></span>
<span data-ttu-id="26e41-124">Указывает ключ шифрования службы для виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="26e41-124">Specifies a service encryption key for the virtual device.</span></span>
<span data-ttu-id="26e41-125">Этот ключ создается при регистрации первого физического устройства в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="26e41-125">This key is generated when the first physical device is registered with a resource.</span></span>

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

### <span data-ttu-id="26e41-126">-SnapshotManagerPassword</span><span class="sxs-lookup"><span data-stu-id="26e41-126">-SnapshotManagerPassword</span></span>
<span data-ttu-id="26e41-127">Указывает пароль диспетчера снимков.</span><span class="sxs-lookup"><span data-stu-id="26e41-127">Specifies the snapshot manager password.</span></span>

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

### <span data-ttu-id="26e41-128">-Часовой пояс</span><span class="sxs-lookup"><span data-stu-id="26e41-128">-TimeZone</span></span>
<span data-ttu-id="26e41-129">Указывает часовой пояс для устройства.</span><span class="sxs-lookup"><span data-stu-id="26e41-129">Specifies a time zone for the device.</span></span>
<span data-ttu-id="26e41-130">Вы можете создать объект **TimeZoneInfo** с помощью метода **GetSystemTimeZone ()** .</span><span class="sxs-lookup"><span data-stu-id="26e41-130">You can create a **TimeZoneInfo** object by using the **GetSystemTimeZone()** method.</span></span>
<span data-ttu-id="26e41-131">Например, эта команда создает объект сведения о часовом поясе для стандартного тихоокеанское время: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span><span class="sxs-lookup"><span data-stu-id="26e41-131">For example, this command creates a time zone information object for Pacific Standard Time: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span></span>

```yaml
Type: TimeZoneInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26e41-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e41-132">CommonParameters</span></span>
<span data-ttu-id="26e41-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="26e41-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e41-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26e41-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e41-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="26e41-135">INPUTS</span></span>

### <span data-ttu-id="26e41-136">TimeZoneInfo</span><span class="sxs-lookup"><span data-stu-id="26e41-136">TimeZoneInfo</span></span>
<span data-ttu-id="26e41-137">Вы можете передать на этот командлет объект **TimeZoneInfo** .</span><span class="sxs-lookup"><span data-stu-id="26e41-137">You can pipe a **TimeZoneInfo** object to this cmdlet.</span></span>

## <span data-ttu-id="26e41-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="26e41-138">OUTPUTS</span></span>

### <span data-ttu-id="26e41-139">DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="26e41-139">DeviceJobDetails</span></span>
<span data-ttu-id="26e41-140">Этот командлет возвращает обновленные сведения об устройстве для виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="26e41-140">This cmdlet returns updated device details for the virtual device.</span></span>

## <span data-ttu-id="26e41-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="26e41-141">NOTES</span></span>

## <span data-ttu-id="26e41-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26e41-142">RELATED LINKS</span></span>

[<span data-ttu-id="26e41-143">New-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="26e41-143">New-AzureStorSimpleVirtualDevice</span></span>](./New-AzureStorSimpleVirtualDevice.md)

[<span data-ttu-id="26e41-144">Set-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="26e41-144">Set-AzureStorSimpleDevice</span></span>](./Set-AzureStorSimpleDevice.md)


