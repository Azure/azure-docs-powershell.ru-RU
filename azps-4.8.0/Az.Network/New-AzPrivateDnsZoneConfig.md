---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszoneconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
ms.openlocfilehash: b80889f1838945f6ba119f539c5badd59b43de61
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079469"
---
# <span data-ttu-id="49c38-101">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="49c38-101">New-AzPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="49c38-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49c38-102">SYNOPSIS</span></span>
<span data-ttu-id="49c38-103">Создание конфигурации зоны DNS для частной группы зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="49c38-103">Creates DNS zone configuration of the private dns zone group.</span></span>

## <span data-ttu-id="49c38-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49c38-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneConfig -Name <String> [-PrivateDnsZoneId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49c38-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49c38-105">DESCRIPTION</span></span>
<span data-ttu-id="49c38-106">С помощью командлета **New-AzPrivateDnsZoneConfig** вы можете создать новый объект конфигурации зоны DNS, который будет установлен в группе зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="49c38-106">The **New-AzPrivateDnsZoneConfig** cmdlet enables you to create a new DNS zone configuration object which will be set on DNS zone group.</span></span>

## <span data-ttu-id="49c38-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49c38-107">EXAMPLES</span></span>

### <span data-ttu-id="49c38-108">Создание конфигурации зоны DNS</span><span class="sxs-lookup"><span data-stu-id="49c38-108">Creates DNS zone configuration</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
```

<span data-ttu-id="49c38-109">В приведенном выше примере создается зона DNS, а затем создается конфигурация зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="49c38-109">The above example creates DNS zone and then creates DNS zone configuration.</span></span> <span data-ttu-id="49c38-110">`New-AzPrivateDnsZone` Командлет доявляется модулем AZ. PrivateDns.</span><span class="sxs-lookup"><span data-stu-id="49c38-110">`New-AzPrivateDnsZone` cmdlet is proveded by module Az.PrivateDns.</span></span>

## <span data-ttu-id="49c38-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49c38-111">PARAMETERS</span></span>

### <span data-ttu-id="49c38-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49c38-112">-DefaultProfile</span></span>
<span data-ttu-id="49c38-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49c38-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49c38-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="49c38-114">-Name</span></span>
<span data-ttu-id="49c38-115">Имя ресурса, уникального в рамках группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="49c38-115">Name of the resource that is unique within a resource group.</span></span>
<span data-ttu-id="49c38-116">Это имя можно использовать для доступа к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="49c38-116">This name can be used to access the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c38-117">-PrivateDnsZoneId</span><span class="sxs-lookup"><span data-stu-id="49c38-117">-PrivateDnsZoneId</span></span>
<span data-ttu-id="49c38-118">Идентификатор ресурса частной зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="49c38-118">The resource id of the private dns zone.</span></span>

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

### <span data-ttu-id="49c38-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49c38-119">CommonParameters</span></span>
<span data-ttu-id="49c38-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49c38-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49c38-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49c38-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49c38-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49c38-122">INPUTS</span></span>

### <span data-ttu-id="49c38-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="49c38-123">None</span></span>

## <span data-ttu-id="49c38-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49c38-124">OUTPUTS</span></span>

### <span data-ttu-id="49c38-125">Microsoft. Azure. Commands. Network. Models. PSPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="49c38-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="49c38-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="49c38-126">NOTES</span></span>

## <span data-ttu-id="49c38-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49c38-127">RELATED LINKS</span></span>
