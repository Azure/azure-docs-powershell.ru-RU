---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
ms.openlocfilehash: 8bc586ea9543c7545e7d24e3bc6d7bc36bb77d49
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234188"
---
# <span data-ttu-id="33735-101">Get-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="33735-101">Get-AzIotHubCertificate</span></span>

## <span data-ttu-id="33735-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33735-102">SYNOPSIS</span></span>
<span data-ttu-id="33735-103">Список всех сертификатов или отдельных сертификатов, содержащихся в Центре Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="33735-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="33735-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="33735-104">SYNTAX</span></span>

### <span data-ttu-id="33735-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="33735-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33735-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="33735-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33735-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="33735-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33735-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="33735-108">DESCRIPTION</span></span>
<span data-ttu-id="33735-109">Подробное описание сертификатов ЦС в Azure IoT Hub см. в https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="33735-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="33735-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="33735-110">EXAMPLES</span></span>

### <span data-ttu-id="33735-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="33735-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="33735-112">Список всех сертификатов в MyIotHub</span><span class="sxs-lookup"><span data-stu-id="33735-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="33735-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="33735-113">Example 2</span></span>
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

<span data-ttu-id="33735-114">Показать сведения о MyCertificate</span><span class="sxs-lookup"><span data-stu-id="33735-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="33735-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33735-115">PARAMETERS</span></span>

### <span data-ttu-id="33735-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="33735-116">-CertificateName</span></span>
<span data-ttu-id="33735-117">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="33735-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="33735-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33735-118">-DefaultProfile</span></span>
<span data-ttu-id="33735-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="33735-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33735-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33735-120">-InputObject</span></span>
<span data-ttu-id="33735-121">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="33735-121">IotHub Object</span></span>

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

### <span data-ttu-id="33735-122">-Name</span><span class="sxs-lookup"><span data-stu-id="33735-122">-Name</span></span>
<span data-ttu-id="33735-123">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="33735-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="33735-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33735-124">-ResourceGroupName</span></span>
<span data-ttu-id="33735-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="33735-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="33735-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33735-126">-ResourceId</span></span>
<span data-ttu-id="33735-127">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="33735-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="33735-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33735-128">CommonParameters</span></span>
<span data-ttu-id="33735-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33735-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33735-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33735-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33735-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="33735-131">INPUTS</span></span>

### <span data-ttu-id="33735-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="33735-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="33735-133">System.String</span><span class="sxs-lookup"><span data-stu-id="33735-133">System.String</span></span>

## <span data-ttu-id="33735-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="33735-134">OUTPUTS</span></span>

### <span data-ttu-id="33735-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="33735-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="33735-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="33735-136">NOTES</span></span>

## <span data-ttu-id="33735-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="33735-137">RELATED LINKS</span></span>
