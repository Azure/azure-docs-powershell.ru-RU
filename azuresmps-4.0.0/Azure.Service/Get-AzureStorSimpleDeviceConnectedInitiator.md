---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 9436E1AB-870F-4717-ABE0-55A90C07F7E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 555ce014bbbf7174b3f7142cf7e2f217317eadc6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076291"
---
# <span data-ttu-id="f7224-101">Get-AzureStorSimpleDeviceConnectedInitiator</span><span class="sxs-lookup"><span data-stu-id="f7224-101">Get-AzureStorSimpleDeviceConnectedInitiator</span></span>

## <span data-ttu-id="f7224-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7224-102">SYNOPSIS</span></span>
<span data-ttu-id="f7224-103">Получение подключений iSCSI, доступных для устройства StorSimple.</span><span class="sxs-lookup"><span data-stu-id="f7224-103">Gets the iSCSI connections available for a StorSimple device.</span></span>

## <span data-ttu-id="f7224-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7224-104">SYNTAX</span></span>

### <span data-ttu-id="f7224-105">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="f7224-105">IdentifyById</span></span>
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f7224-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="f7224-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7224-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7224-107">DESCRIPTION</span></span>
<span data-ttu-id="f7224-108">Командлет **Get-AzureStorSimpleDeviceConnectedInitiator** получает список доступных подключений iSCSI для устройства StorSimple.</span><span class="sxs-lookup"><span data-stu-id="f7224-108">The **Get-AzureStorSimpleDeviceConnectedInitiator** cmdlet gets a list of the iSCSI connections available for a StorSimple device.</span></span>
<span data-ttu-id="f7224-109">Объекты подключения iSCSI, возвращаемые этим командлетом, содержат следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="f7224-109">The iSCSI connection objects that this cmdlet returns contain the following properties:</span></span>

- <span data-ttu-id="f7224-110">**AcrInstanceId**</span><span class="sxs-lookup"><span data-stu-id="f7224-110">**AcrInstanceId**</span></span>
- <span data-ttu-id="f7224-111">**AcrName**</span><span class="sxs-lookup"><span data-stu-id="f7224-111">**AcrName**</span></span>
- <span data-ttu-id="f7224-112">**AllowedVolumeNames**</span><span class="sxs-lookup"><span data-stu-id="f7224-112">**AllowedVolumeNames**</span></span>
- <span data-ttu-id="f7224-113">**InitiatorAddress**</span><span class="sxs-lookup"><span data-stu-id="f7224-113">**InitiatorAddress**</span></span>
- <span data-ttu-id="f7224-114">**Приклад**</span><span class="sxs-lookup"><span data-stu-id="f7224-114">**Interfaces**</span></span>
- <span data-ttu-id="f7224-115">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="f7224-115">**Iqn**</span></span>
- <span data-ttu-id="f7224-116">**IscsiConnectionId**</span><span class="sxs-lookup"><span data-stu-id="f7224-116">**IscsiConnectionId**</span></span>

<span data-ttu-id="f7224-117">Этот командлет получает объект подключения только в том случае, если для устройства включены подключения iSCSI.</span><span class="sxs-lookup"><span data-stu-id="f7224-117">This cmdlet gets connection object only if iSCSI connections are turned on for the device.</span></span>
<span data-ttu-id="f7224-118">По умолчанию подключения отключены.</span><span class="sxs-lookup"><span data-stu-id="f7224-118">By default, connections are turned off.</span></span>

## <span data-ttu-id="f7224-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7224-119">EXAMPLES</span></span>

### <span data-ttu-id="f7224-120">Пример 1: получение всех подключений для устройства</span><span class="sxs-lookup"><span data-stu-id="f7224-120">Example 1: Get all connections for a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: bec615b9-79ab-4671-88b0-287adeb6bf68_PS
VERBOSE: ClientRequestId: ef976c58-2660-41c8-aa15-c84e70c9d01c_PS
VERBOSE: ClientRequestId: 9b306b96-8e76-47ed-beda-d3bd2fb2bb82_PS
VERBOSE: ClientRequestId: 0f4fc743-0b60-45da-a45a-27f4b0f32bd2_PS

AcrInstanceId      : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
AcrName            : Contoso63-AppVm
AllowedVolumeNames : {Policyvolume1_Default}
InitiatorAddress   : 
Interfaces         : {Data0}
Iqn                : iqn10
IscsiConnectionId  : cfc144cb-00f1-44b1-9655-80b431f2161b

VERBOSE: 1 Iscsi Connection found!
```

<span data-ttu-id="f7224-121">Эта команда получает все подключения iSCSI для устройства с именем Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="f7224-121">This command gets all iSCSI connections for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="f7224-122">Эта команда возвращает подключения только в том случае, если для устройства включены подключения.</span><span class="sxs-lookup"><span data-stu-id="f7224-122">This command returns connections only if connections are turned on for the device.</span></span>

## <span data-ttu-id="f7224-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7224-123">PARAMETERS</span></span>

### <span data-ttu-id="f7224-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="f7224-124">-DeviceId</span></span>
<span data-ttu-id="f7224-125">Указывает ИД экземпляра устройства StorSimple, из которого требуется получить инициаторы iSCSI.</span><span class="sxs-lookup"><span data-stu-id="f7224-125">Specifies the instance ID of the StorSimple device from which to get iSCSI initiators.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7224-126">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="f7224-126">-DeviceName</span></span>
<span data-ttu-id="f7224-127">Указывает имя устройства StorSimple, для которого требуется получить инициаторы iSCSI.</span><span class="sxs-lookup"><span data-stu-id="f7224-127">Specifies the name of the StorSimple device from which to get iSCSI initiators.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7224-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="f7224-128">-Profile</span></span>
<span data-ttu-id="f7224-129">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="f7224-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="f7224-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7224-130">CommonParameters</span></span>
<span data-ttu-id="f7224-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7224-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7224-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7224-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7224-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7224-133">INPUTS</span></span>

### <span data-ttu-id="f7224-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="f7224-134">None</span></span>

## <span data-ttu-id="f7224-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7224-135">OUTPUTS</span></span>

### <span data-ttu-id="f7224-136">Список\<IscsiConnection\></span><span class="sxs-lookup"><span data-stu-id="f7224-136">List\<IscsiConnection\></span></span>
<span data-ttu-id="f7224-137">Этот командлет возвращает объект подключения iSCSI, который включает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="f7224-137">This cmdlet returns an iSCSI connection object that contains the following properties:</span></span> 

- <span data-ttu-id="f7224-138">**AcrInstanceId**</span><span class="sxs-lookup"><span data-stu-id="f7224-138">**AcrInstanceId**</span></span>
- <span data-ttu-id="f7224-139">**AcrName**</span><span class="sxs-lookup"><span data-stu-id="f7224-139">**AcrName**</span></span>
- <span data-ttu-id="f7224-140">**AllowedVolumeNames**</span><span class="sxs-lookup"><span data-stu-id="f7224-140">**AllowedVolumeNames**</span></span>
- <span data-ttu-id="f7224-141">**InitiatorAddress**</span><span class="sxs-lookup"><span data-stu-id="f7224-141">**InitiatorAddress**</span></span>
- <span data-ttu-id="f7224-142">**Приклад**</span><span class="sxs-lookup"><span data-stu-id="f7224-142">**Interfaces**</span></span>
- <span data-ttu-id="f7224-143">**Изменение**</span><span class="sxs-lookup"><span data-stu-id="f7224-143">**Iqn**</span></span>
- <span data-ttu-id="f7224-144">**IscsiConnectionId**</span><span class="sxs-lookup"><span data-stu-id="f7224-144">**IscsiConnectionId**</span></span>

## <span data-ttu-id="f7224-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7224-145">NOTES</span></span>

## <span data-ttu-id="f7224-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7224-146">RELATED LINKS</span></span>

[<span data-ttu-id="f7224-147">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="f7224-147">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)


