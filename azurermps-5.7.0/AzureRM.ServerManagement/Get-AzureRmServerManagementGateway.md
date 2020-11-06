---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: C579BF90-FD8B-4384-96EB-46154E308492
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/get-azurermservermanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
ms.openlocfilehash: 9dc7e38cf169e79ec7dae279c6fa09f069b1ade7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557164"
---
# <span data-ttu-id="493d5-101">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="493d5-101">Get-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="493d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="493d5-102">SYNOPSIS</span></span>
<span data-ttu-id="493d5-103">Получает один или несколько шлюзов управления сервером.</span><span class="sxs-lookup"><span data-stu-id="493d5-103">Gets one or more Server Management Gateways.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="493d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="493d5-104">SYNTAX</span></span>

### <span data-ttu-id="493d5-105">Params (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="493d5-105">NoParams (Default)</span></span>
```
Get-AzureRmServerManagementGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="493d5-106">Many-ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="493d5-106">Many-ByResourceGroup</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="493d5-107">Single-ByName</span><span class="sxs-lookup"><span data-stu-id="493d5-107">Single-ByName</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="493d5-108">Single-ByObject</span><span class="sxs-lookup"><span data-stu-id="493d5-108">Single-ByObject</span></span>
```
Get-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="493d5-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="493d5-109">DESCRIPTION</span></span>
<span data-ttu-id="493d5-110">Командлет **Get-AzureRmServerManagementGateway** получает один или несколько шлюзов управления Azure Server.</span><span class="sxs-lookup"><span data-stu-id="493d5-110">The **Get-AzureRmServerManagementGateway** cmdlet gets one or more Azure Server Management Gateways.</span></span>

## <span data-ttu-id="493d5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="493d5-111">EXAMPLES</span></span>

### <span data-ttu-id="493d5-112">Пример 1: получение всех шлюзов в подписке</span><span class="sxs-lookup"><span data-stu-id="493d5-112">Example 1: Get all gateways in a subscription</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
groupOne       centralus      Off          mygateway
groupOne       centralus      Off          othergateway
groupTwo       centralus      On           privategateway
```

<span data-ttu-id="493d5-113">Эта команда получает все шлюзы управления серверами в подписке.</span><span class="sxs-lookup"><span data-stu-id="493d5-113">This command gets all Server Management Gateways in the subscription.</span></span>

### <span data-ttu-id="493d5-114">Пример 2: получение шлюзов в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="493d5-114">Example 2: Get gateways in a resource group</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway -ResourceGroupName "Group001"
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
myGroup        centralus      Off          mygateway
```

<span data-ttu-id="493d5-115">Эта команда получает все шлюзы управления серверами, которые принадлежат группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="493d5-115">This command gets all Server Management Gateways that belong to the resource group named Group001.</span></span>

### <span data-ttu-id="493d5-116">Пример 3: получение всех установленных экземпляров шлюза</span><span class="sxs-lookup"><span data-stu-id="493d5-116">Example 3: Get all installed instances of a gateway</span></span>
```
PS C:\>(Get-AzureRmServerManagementGateway -ResourceGroupName "Group002" -GatewayName "Gateway01").Instances
Name             Installed              Version         Operating System
----             ---------              -------         ----------------
GATEWAYPC        4/13/2016 6:35:04 PM   1.0.1104.0      Microsoft Windows 10 Enterprise
```

<span data-ttu-id="493d5-117">Эта команда получает все экземпляры шлюза управления сервером с именем Gateway01, которые принадлежат группе ресурсов с именем Group002.</span><span class="sxs-lookup"><span data-stu-id="493d5-117">This command gets all instances of a Server Management Gateway named Gateway01 that belong to the resource group named Group002.</span></span>

## <span data-ttu-id="493d5-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="493d5-118">PARAMETERS</span></span>

### <span data-ttu-id="493d5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="493d5-119">-DefaultProfile</span></span>
<span data-ttu-id="493d5-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="493d5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="493d5-121">-Gateway</span><span class="sxs-lookup"><span data-stu-id="493d5-121">-Gateway</span></span>
<span data-ttu-id="493d5-122">Указывает шлюз, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="493d5-122">Specifies a gateway that this cmdlet gets.</span></span>

<span data-ttu-id="493d5-123">Командлет использует параметры *ResourceGroupName* и *GatewayName* с помощью указанного шлюза для выполнения действия.</span><span class="sxs-lookup"><span data-stu-id="493d5-123">The cmdlet uses the *ResourceGroupName* and *GatewayName* parameters through the specified Gateway to perform the action.</span></span>

<span data-ttu-id="493d5-124">Если указан этот параметр, этот командлет будет включать подробное состояние шлюза.</span><span class="sxs-lookup"><span data-stu-id="493d5-124">When this parameter is specified, this cmdlet will include detailed status for the gateway.</span></span>

```yaml
Type: Gateway
Parameter Sets: Single-ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="493d5-125">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="493d5-125">-GatewayName</span></span>
<span data-ttu-id="493d5-126">Указывает имя шлюза управления сервером, для которого этот командлет получает шлюз.</span><span class="sxs-lookup"><span data-stu-id="493d5-126">Specifies the name of the Server Management Gateway for which this cmdlet gets gate.</span></span>

<span data-ttu-id="493d5-127">При указании параметра *GatewayName* этот командлет будет включать подробное состояние шлюза.</span><span class="sxs-lookup"><span data-stu-id="493d5-127">When you specify the *GatewayName* parameter, this cmdlet will include detailed status on the gateway.</span></span>

```yaml
Type: String
Parameter Sets: Single-ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="493d5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="493d5-128">-ResourceGroupName</span></span>
<span data-ttu-id="493d5-129">Указывает имя группы ресурсов, для которой этот командлет получает шлюзы.</span><span class="sxs-lookup"><span data-stu-id="493d5-129">Specifies the name of the resource group for which this cmdlet gets gateways.</span></span>

```yaml
Type: String
Parameter Sets: Many-ByResourceGroup, Single-ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="493d5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="493d5-130">CommonParameters</span></span>
<span data-ttu-id="493d5-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="493d5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="493d5-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="493d5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="493d5-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="493d5-133">INPUTS</span></span>

### <span data-ttu-id="493d5-134">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="493d5-134">Gateway</span></span>
<span data-ttu-id="493d5-135">Параметр Gateway принимает от конвейера значение типа Gateway.</span><span class="sxs-lookup"><span data-stu-id="493d5-135">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="493d5-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="493d5-136">OUTPUTS</span></span>

### <span data-ttu-id="493d5-137">Microsoft. Azure. Commands. ServerManagement. Model. Gateway</span><span class="sxs-lookup"><span data-stu-id="493d5-137">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="493d5-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="493d5-138">NOTES</span></span>
* <span data-ttu-id="493d5-139">Если этот командлет используется без параметров, будут возвращены все шлюзы, связанные с подпиской.</span><span class="sxs-lookup"><span data-stu-id="493d5-139">If this cmdlet is use without parameters, it will return all the gateways associated with the subscription.</span></span>

## <span data-ttu-id="493d5-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="493d5-140">RELATED LINKS</span></span>

[<span data-ttu-id="493d5-141">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="493d5-141">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)

[<span data-ttu-id="493d5-142">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="493d5-142">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


