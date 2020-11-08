---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
ms.openlocfilehash: b21fe2cc51668548d4fedc8eb6fc9404d5626a41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235516"
---
# <span data-ttu-id="5badf-101">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="5badf-101">Get-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="5badf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5badf-102">SYNOPSIS</span></span>
<span data-ttu-id="5badf-103">Получить или просмотреть список сайтов, подключенных к ресурсам виртуального устройства сети (-ов).</span><span class="sxs-lookup"><span data-stu-id="5badf-103">Get or List sites connected to Network Virtual Appliance resource(s).</span></span>

## <span data-ttu-id="5badf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5badf-104">SYNTAX</span></span>

### <span data-ttu-id="5badf-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5badf-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzVirtualApplianceSite [-Name <String>] [-NetworkVirtualApplianceId <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5badf-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5badf-106">ResourceIdParameterSet</span></span>
```
Get-AzVirtualApplianceSite -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5badf-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5badf-107">DESCRIPTION</span></span>
<span data-ttu-id="5badf-108">Get-AzVirtualApplianceSite возвращает сайты, подключенные к одному или нескольким сетевым ресурсам сетевого устройства, и перечисляет их.</span><span class="sxs-lookup"><span data-stu-id="5badf-108">The Get-AzVirtualApplianceSite gets or lists sites connected to one or more Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="5badf-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5badf-109">EXAMPLES</span></span>

### <span data-ttu-id="5badf-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5badf-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -Name testsite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite
```

<span data-ttu-id="5badf-111">Получение ресурса сайта виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="5badf-111">Get a Virtual Appliance site resource.</span></span>

### <span data-ttu-id="5badf-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5badf-112">Example 2</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite

AddressPrefix     : 10.0.2.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite2
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite2
```

<span data-ttu-id="5badf-113">Перечислите ресурсы сайта виртуального устройства в сетевом виртуальном устройстве.</span><span class="sxs-lookup"><span data-stu-id="5badf-113">List Virtual Appliance site resources in a Network Virtual Appliance.</span></span>


## <span data-ttu-id="5badf-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5badf-114">PARAMETERS</span></span>

### <span data-ttu-id="5badf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5badf-115">-DefaultProfile</span></span>
<span data-ttu-id="5badf-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5badf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5badf-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5badf-117">-Name</span></span>
<span data-ttu-id="5badf-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="5badf-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5badf-119">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="5badf-119">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="5badf-120">Виртуальное сетевое устройство, к которому подключен сайт.</span><span class="sxs-lookup"><span data-stu-id="5badf-120">The Network Virtual Appliance that the site is attached.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5badf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5badf-121">-ResourceGroupName</span></span>
<span data-ttu-id="5badf-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5badf-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5badf-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5badf-123">-ResourceId</span></span>
<span data-ttu-id="5badf-124">Идентификатор ресурса сайта виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="5badf-124">The resource Id of the Virtual Appliance Site.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5badf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5badf-125">CommonParameters</span></span>
<span data-ttu-id="5badf-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5badf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5badf-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5badf-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5badf-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5badf-128">INPUTS</span></span>

### <span data-ttu-id="5badf-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5badf-129">System.String</span></span>

## <span data-ttu-id="5badf-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5badf-130">OUTPUTS</span></span>

### <span data-ttu-id="5badf-131">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="5badf-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="5badf-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="5badf-132">NOTES</span></span>

## <span data-ttu-id="5badf-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5badf-133">RELATED LINKS</span></span>
