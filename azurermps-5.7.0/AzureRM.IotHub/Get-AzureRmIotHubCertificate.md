---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificate.md
ms.openlocfilehash: 6b537811f47399d3be6b5d6485a492f7623a84c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564887"
---
# <span data-ttu-id="2b030-101">Get-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="2b030-101">Get-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="2b030-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b030-102">SYNOPSIS</span></span>
<span data-ttu-id="2b030-103">Список всех сертификатов или определенного сертификата, входящего в состав центра Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="2b030-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b030-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b030-104">SYNTAX</span></span>

### <span data-ttu-id="2b030-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2b030-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b030-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2b030-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b030-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2b030-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b030-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b030-108">DESCRIPTION</span></span>
<span data-ttu-id="2b030-109">Подробное описание сертификатов ЦС в центре Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="2b030-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="2b030-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b030-110">EXAMPLES</span></span>

### <span data-ttu-id="2b030-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2b030-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="2b030-112">Список всех сертификатов в MyIotHub</span><span class="sxs-lookup"><span data-stu-id="2b030-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="2b030-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2b030-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate"

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

<span data-ttu-id="2b030-114">Показать подробные сведения о MyCertificate</span><span class="sxs-lookup"><span data-stu-id="2b030-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="2b030-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b030-115">PARAMETERS</span></span>

### <span data-ttu-id="2b030-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="2b030-116">-CertificateName</span></span>
<span data-ttu-id="2b030-117">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="2b030-117">Name of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b030-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b030-118">-DefaultProfile</span></span>
<span data-ttu-id="2b030-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b030-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b030-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b030-120">-InputObject</span></span>
<span data-ttu-id="2b030-121">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="2b030-121">IotHub Object</span></span>

```yaml
Type: PSIotHub
Parameter Sets: InputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b030-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2b030-122">-Name</span></span>
<span data-ttu-id="2b030-123">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="2b030-123">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b030-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b030-124">-ResourceGroupName</span></span>
<span data-ttu-id="2b030-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2b030-125">Name of the Resource Group</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b030-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b030-126">-ResourceId</span></span>
<span data-ttu-id="2b030-127">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="2b030-127">IotHub Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b030-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b030-128">CommonParameters</span></span>
<span data-ttu-id="2b030-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b030-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b030-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b030-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b030-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b030-131">INPUTS</span></span>

### <span data-ttu-id="2b030-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2b030-132">System.String</span></span>

## <span data-ttu-id="2b030-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b030-133">OUTPUTS</span></span>

### <span data-ttu-id="2b030-134">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="2b030-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>
<span data-ttu-id="2b030-135">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription, Microsoft. Azure. Commands. IotHub, Version = 3.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="2b030-135">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription, Microsoft.Azure.Commands.IotHub, Version=3.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2b030-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b030-136">NOTES</span></span>

## <span data-ttu-id="2b030-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b030-137">RELATED LINKS</span></span>

