---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkservicetag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
ms.openlocfilehash: c511dc6eba981708557797dc657e4626621f9131
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249858"
---
# <span data-ttu-id="d9f49-101">Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="d9f49-101">Get-AzNetworkServiceTag</span></span>

## <span data-ttu-id="d9f49-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d9f49-102">SYNOPSIS</span></span>
<span data-ttu-id="d9f49-103">Получает список ресурсов с данными тега обслуживания.</span><span class="sxs-lookup"><span data-stu-id="d9f49-103">Gets the list of service tag information resources.</span></span>

## <span data-ttu-id="d9f49-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d9f49-104">SYNTAX</span></span>

```
Get-AzNetworkServiceTag -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9f49-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9f49-105">DESCRIPTION</span></span>
<span data-ttu-id="d9f49-106">Командлет **Get-AzNetworkServiceTag** получает список ресурсов с данными об тегах обслуживания.</span><span class="sxs-lookup"><span data-stu-id="d9f49-106">The **Get-AzNetworkServiceTag** cmdlet gets the list of service tag information resources.</span></span>

<span data-ttu-id="d9f49-107">Обратите внимание, что указанные вами сведения о регионе Azure будут использоваться в качестве ссылки на версию (но не в качестве фильтра на основе расположения).</span><span class="sxs-lookup"><span data-stu-id="d9f49-107">Please note that the Azure region information you specify will be used as a reference for version (not as a filter based on location).</span></span> <span data-ttu-id="d9f49-108">Например, даже если вы укажете `-Location eastus2` список служебных тегов с подробными сведениями о них в разных регионах, но только в облаке, к которому относится ваша подписка (например, "общедоступный", "правительство США", "Китайский" или "Германия").</span><span class="sxs-lookup"><span data-stu-id="d9f49-108">For example, even if you specify `-Location eastus2` you will get the list of service tags with prefix details across all regions but limited to the cloud that your subscription belongs to (i.e. Public, US government, China or Germany).</span></span>

## <span data-ttu-id="d9f49-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d9f49-109">EXAMPLES</span></span>

### <span data-ttu-id="d9f49-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d9f49-110">Example 1</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags

Name         : Public
Id           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/providers/Microsoft.Network/serviceTags/Public
Type         : Microsoft.Network/serviceTags
ChangeNumber : 63
Cloud        : Public
Values       : {ApiManagement, ApiManagement.AustraliaCentral, ApiManagement.AustraliaCentral2, ApiManagement.AustraliaEast...}

PS C:\> $serviceTags.Values

Name             : ApiManagement
System Service   : AzureApiManagement
Address Prefixes : {13.64.39.16/32, 13.66.138.92/31, 13.66.140.176/28, 13.67.8.108/31...}
Change Number    : 7

Name             : ApiManagement.AustraliaCentral
System Service   : AzureApiManagement
Region           : australiacentral
Address Prefixes : {20.36.106.68/31, 20.36.107.176/28}
Change Number    : 2

Name             : ApiManagement.AustraliaCentral2
System Service   : AzureApiManagement
Region           : australiacentral2
Address Prefixes : {20.36.114.20/31, 20.36.115.128/28}
Change Number    : 2

Name             : ApiManagement.AustraliaEast
System Service   : AzureApiManagement
Region           : australiaeast
Address Prefixes : {13.70.72.28/31, 13.70.72.240/28, 13.75.217.184/32, 13.75.221.78/32...}
Change Number    : 3

Name             : ApiManagement.AustraliaSoutheast
System Service   : AzureApiManagement
Region           : australiasoutheast
Address Prefixes : {13.77.50.68/31, 13.77.52.224/28}
Change Number    : 2

...
```

<span data-ttu-id="d9f49-111">Команда получает список ресурсов с данными тега обслуживания и сохраняет их в переменной `serviceTags` .</span><span class="sxs-lookup"><span data-stu-id="d9f49-111">The command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>

### <span data-ttu-id="d9f49-112">Пример 2: получение префиксов для всех адресов для AzureSQL</span><span class="sxs-lookup"><span data-stu-id="d9f49-112">Example 2: Get all address prefixes for AzureSQL</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $sql = $serviceTags.Values | Where-Object { $_.Name -eq "Sql" }
PS C:\> $sql

Name             : Sql
System Service   : AzureSQL
Address Prefixes : {13.65.31.249/32, 13.65.39.207/32, 13.65.85.183/32, 13.65.200.105/32...}
Change Number    : 18

PS C:\> $sql.Properties.AddressPrefixes.Count
644
PS C:\> $sql.Properties.AddressPrefixes
13.65.31.249/32
13.65.39.207/32
13.65.85.183/32
13.65.200.105/32
13.65.209.243/32
...
```

<span data-ttu-id="d9f49-113">Первая команда получает список ресурсов с данными тега обслуживания и сохраняет их в переменной `serviceTags` .</span><span class="sxs-lookup"><span data-stu-id="d9f49-113">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="d9f49-114">Вторая команда фильтрует список, чтобы выбрать информационный ресурс для SQL.</span><span class="sxs-lookup"><span data-stu-id="d9f49-114">The second command filters the list to select information resource for Sql.</span></span>

### <span data-ttu-id="d9f49-115">Пример 3: получение ресурса сведений о тегах обслуживания хранилища для Западов США 2</span><span class="sxs-lookup"><span data-stu-id="d9f49-115">Example 3: Get Storage's service tag information resource for West US 2</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags.Values | Where-Object { $_.Name -eq "Storage.WestUS2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5

PS C:\> $serviceTags.Values | Where-Object { $_.Name -like "Storage*" -and $_.Properties.Region -eq "westus2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5

PS C:\> $serviceTags.Values | Where-Object { $_.Properties.SystemService -eq "AzureStorage" -and $_.Properties.Region -eq "westus2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5
```

<span data-ttu-id="d9f49-116">Первая команда получает список ресурсов с данными тега обслуживания и сохраняет их в переменной `serviceTags` .</span><span class="sxs-lookup"><span data-stu-id="d9f49-116">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="d9f49-117">Следующие команды показывают различные способы фильтрации списка для выбора сведений о тегах обслуживания для хранения в Западная часть US 2.</span><span class="sxs-lookup"><span data-stu-id="d9f49-117">The following commands show various way to filter the list to select service tag information for Storage in West US 2.</span></span>

### <span data-ttu-id="d9f49-118">Пример 4: получение всех ресурсов глобальных данных тега Global Service</span><span class="sxs-lookup"><span data-stu-id="d9f49-118">Example 4: Get all global service tag information resources</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags.Values | Where-Object { -not $_.Properties.Region }


Name             : ApiManagement
System Service   : AzureApiManagement
Address Prefixes : {13.64.39.16/32, 13.66.138.92/31, 13.66.140.176/28, 13.67.8.108/31...}
Change Number    : 7

Name             : AppService
System Service   : AzureAppService
Address Prefixes : {13.64.73.110/32, 13.65.30.245/32, 13.65.37.122/32, 13.65.39.165/32...}
Change Number    : 13

Name             : AppServiceManagement
System Service   : AzureAppServiceManagement
Address Prefixes : {13.64.115.203/32, 13.66.140.0/26, 13.67.8.128/26, 13.69.64.128/26...}
Change Number    : 7

Name             : AzureActiveDirectory
System Service   : AzureAD
Address Prefixes : {13.64.151.161/32, 13.66.141.64/27, 13.67.9.224/27, 13.67.50.224/29...}
Change Number    : 3

Name             : AzureActiveDirectoryDomainServices
System Service   : AzureIdentity
Address Prefixes : {13.64.151.161/32, 13.66.141.64/27, 13.67.9.224/27, 13.69.66.160/27...}
Change Number    : 2

...
```

<span data-ttu-id="d9f49-119">Первая команда получает список ресурсов с данными тега обслуживания и сохраняет их в переменной `serviceTags` .</span><span class="sxs-lookup"><span data-stu-id="d9f49-119">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="d9f49-120">Вторая команда фильтрует список, чтобы выбрать только те элементы, для которых не установлен регион.</span><span class="sxs-lookup"><span data-stu-id="d9f49-120">The second command filters the list to select only those without set region.</span></span>

## <span data-ttu-id="d9f49-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d9f49-121">PARAMETERS</span></span>

### <span data-ttu-id="d9f49-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9f49-122">-DefaultProfile</span></span>
<span data-ttu-id="d9f49-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d9f49-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9f49-124">-Location</span><span class="sxs-lookup"><span data-stu-id="d9f49-124">-Location</span></span>
<span data-ttu-id="d9f49-125">Расположение, которое будет использоваться в качестве ссылки на версию (но не в качестве фильтра на основе расположения, вы получите список служебных тегов с подробными сведениями по всем регионам, но только в облаке, к которому относится ваша подписка).</span><span class="sxs-lookup"><span data-stu-id="d9f49-125">The location that will be used as a reference for version (not as a filter based on location, you will get the list of service tags with prefix details across all regions but limited to the cloud that your subscription belongs to).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9f49-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9f49-126">CommonParameters</span></span>
<span data-ttu-id="d9f49-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d9f49-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9f49-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9f49-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9f49-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d9f49-129">INPUTS</span></span>

### <span data-ttu-id="d9f49-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d9f49-130">System.String</span></span>

## <span data-ttu-id="d9f49-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9f49-131">OUTPUTS</span></span>

### <span data-ttu-id="d9f49-132">Microsoft. Azure. Commands. Network. Models. PSNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="d9f49-132">Microsoft.Azure.Commands.Network.Models.PSNetworkServiceTag</span></span>

## <span data-ttu-id="d9f49-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="d9f49-133">NOTES</span></span>

## <span data-ttu-id="d9f49-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9f49-134">RELATED LINKS</span></span>
