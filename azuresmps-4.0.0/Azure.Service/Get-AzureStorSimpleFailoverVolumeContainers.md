---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BABBA19E-5833-452C-9E36-811EAE7C20F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb326281058f0ff9280c4b87c0530241ece801e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075561"
---
# <span data-ttu-id="235a4-101">Get-AzureStorSimpleFailoverVolumeContainers</span><span class="sxs-lookup"><span data-stu-id="235a4-101">Get-AzureStorSimpleFailoverVolumeContainers</span></span>

## <span data-ttu-id="235a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="235a4-102">SYNOPSIS</span></span>
<span data-ttu-id="235a4-103">Возвращает группы контейнера тома для отработки отказа устройства.</span><span class="sxs-lookup"><span data-stu-id="235a4-103">Gets the volume container groups for device failover.</span></span>

## <span data-ttu-id="235a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="235a4-104">SYNTAX</span></span>

### <span data-ttu-id="235a4-105">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="235a4-105">IdentifyById</span></span>
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="235a4-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="235a4-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="235a4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="235a4-107">DESCRIPTION</span></span>
<span data-ttu-id="235a4-108">Командлет **Get-AzureStorSimpleFailoverVolumeContainers** получает группы контейнеров томов для отработки отказа на устройстве.</span><span class="sxs-lookup"><span data-stu-id="235a4-108">The **Get-AzureStorSimpleFailoverVolumeContainers** cmdlet gets the volume container groups for device failover.</span></span>
<span data-ttu-id="235a4-109">Передайте одну группу **VolumeContainer** или массив групп **VolumeContainer** в командлет **Start-AzureStorSimpleDeviceFailover** .</span><span class="sxs-lookup"><span data-stu-id="235a4-109">Pass a single **VolumeContainer** group or an array of **VolumeContainer** groups to the **Start-AzureStorSimpleDeviceFailover** cmdlet.</span></span>
<span data-ttu-id="235a4-110">Отработка отказа подходит только для групп со значением $True для свойства **IsDCGroupEligibleForDR** .</span><span class="sxs-lookup"><span data-stu-id="235a4-110">Only groups that have a value of $True for the **IsDCGroupEligibleForDR** property are eligible for failover.</span></span>

## <span data-ttu-id="235a4-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="235a4-111">EXAMPLES</span></span>

### <span data-ttu-id="235a4-112">Пример 1: получение контейнеров отказоустойчивого тома</span><span class="sxs-lookup"><span data-stu-id="235a4-112">Example 1: Get failover volume containers</span></span>
```
PS C:\>Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7"

DCGroup                    IneligibilityMessage          IsDCGroupEligibleForDR
-------                    --------------------          ----------------------
{VolumeContainer1889078...                                                 True
{VC_01}                    No cloud snapshot found                        False
{VolumeContainer7306959}   No cloud snapshot found                        False
{VolumeContainer407850151} No cloud snapshot found                        False
```

<span data-ttu-id="235a4-113">Эта команда получает контейнеры отказоустойчивого тома.</span><span class="sxs-lookup"><span data-stu-id="235a4-113">This command gets failover volume containers.</span></span>
<span data-ttu-id="235a4-114">Для отработки отказа устройства можно использовать только DCGroups со значением $True для свойства **IsDCGroupEligibleForDR** .</span><span class="sxs-lookup"><span data-stu-id="235a4-114">Only the DCGroups that have a value of $True for the **IsDCGroupEligibleForDR** property can be used for device failover.</span></span>

## <span data-ttu-id="235a4-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="235a4-115">PARAMETERS</span></span>

### <span data-ttu-id="235a4-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="235a4-116">-DeviceId</span></span>
<span data-ttu-id="235a4-117">Указывает ИД экземпляра устройства StorSimple, на котором нужно выполнить командлет.</span><span class="sxs-lookup"><span data-stu-id="235a4-117">Specifies the instance ID of the StorSimple device on which to run the cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235a4-118">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="235a4-118">-DeviceName</span></span>
<span data-ttu-id="235a4-119">Указывает имя устройства StorSimple, на котором будет выполняться командлет.</span><span class="sxs-lookup"><span data-stu-id="235a4-119">Specifies the name of the StorSimple device on which to run the cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235a4-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="235a4-120">-Profile</span></span>
<span data-ttu-id="235a4-121">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="235a4-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="235a4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="235a4-122">CommonParameters</span></span>
<span data-ttu-id="235a4-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="235a4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="235a4-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="235a4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="235a4-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="235a4-125">INPUTS</span></span>

## <span data-ttu-id="235a4-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="235a4-126">OUTPUTS</span></span>

### <span data-ttu-id="235a4-127">Оставлял\<DataContainerGroup\></span><span class="sxs-lookup"><span data-stu-id="235a4-127">IList\<DataContainerGroup\></span></span>
<span data-ttu-id="235a4-128">Этот командлет возвращает список групп **VolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="235a4-128">This cmdlet returns a list of **VolumeContainer** groups.</span></span>

## <span data-ttu-id="235a4-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="235a4-129">NOTES</span></span>

## <span data-ttu-id="235a4-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="235a4-130">RELATED LINKS</span></span>

[<span data-ttu-id="235a4-131">Start-AzureStorSimpleDeviceFailoverJob</span><span class="sxs-lookup"><span data-stu-id="235a4-131">Start-AzureStorSimpleDeviceFailoverJob</span></span>](./Start-AzureStorSimpleDeviceFailoverJob.md)

[<span data-ttu-id="235a4-132">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="235a4-132">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)


