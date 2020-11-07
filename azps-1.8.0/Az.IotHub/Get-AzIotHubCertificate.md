---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
ms.openlocfilehash: 5a8d9c4240ed71b3e5395a3b27927c9477051665
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900366"
---
# <span data-ttu-id="15782-101">Get-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="15782-101">Get-AzIotHubCertificate</span></span>

## <span data-ttu-id="15782-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15782-102">SYNOPSIS</span></span>
<span data-ttu-id="15782-103">Список всех сертификатов или определенного сертификата, входящего в состав центра Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="15782-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="15782-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15782-104">SYNTAX</span></span>

### <span data-ttu-id="15782-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="15782-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15782-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="15782-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15782-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="15782-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15782-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15782-108">DESCRIPTION</span></span>
<span data-ttu-id="15782-109">Подробное описание сертификатов ЦС в центре Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="15782-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="15782-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15782-110">EXAMPLES</span></span>

### <span data-ttu-id="15782-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="15782-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="15782-112">Список всех сертификатов в MyIotHub</span><span class="sxs-lookup"><span data-stu-id="15782-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="15782-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="15782-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="15782-114">Показать подробные сведения о MyCertificate</span><span class="sxs-lookup"><span data-stu-id="15782-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="15782-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15782-115">PARAMETERS</span></span>

### <span data-ttu-id="15782-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="15782-116">-CertificateName</span></span>
<span data-ttu-id="15782-117">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="15782-117">Name of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15782-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15782-118">-DefaultProfile</span></span>
<span data-ttu-id="15782-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15782-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15782-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15782-120">-InputObject</span></span>
<span data-ttu-id="15782-121">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="15782-121">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15782-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="15782-122">-Name</span></span>
<span data-ttu-id="15782-123">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="15782-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15782-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15782-124">-ResourceGroupName</span></span>
<span data-ttu-id="15782-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="15782-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15782-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15782-126">-ResourceId</span></span>
<span data-ttu-id="15782-127">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="15782-127">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15782-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15782-128">CommonParameters</span></span>
<span data-ttu-id="15782-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15782-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15782-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15782-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15782-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15782-131">INPUTS</span></span>

### <span data-ttu-id="15782-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="15782-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="15782-133">System. String</span><span class="sxs-lookup"><span data-stu-id="15782-133">System.String</span></span>

## <span data-ttu-id="15782-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15782-134">OUTPUTS</span></span>

### <span data-ttu-id="15782-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="15782-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="15782-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="15782-136">NOTES</span></span>

## <span data-ttu-id="15782-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15782-137">RELATED LINKS</span></span>
