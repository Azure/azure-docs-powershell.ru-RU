---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszoneconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
ms.openlocfilehash: b80889f1838945f6ba119f539c5badd59b43de61
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248835"
---
# <span data-ttu-id="2081e-101">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="2081e-101">New-AzPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="2081e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2081e-102">SYNOPSIS</span></span>
<span data-ttu-id="2081e-103">Создание конфигурации зоны DNS для частной группы зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="2081e-103">Creates DNS zone configuration of the private dns zone group.</span></span>

## <span data-ttu-id="2081e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2081e-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneConfig -Name <String> [-PrivateDnsZoneId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2081e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2081e-105">DESCRIPTION</span></span>
<span data-ttu-id="2081e-106">С помощью командлета **New-AzPrivateDnsZoneConfig** вы можете создать новый объект конфигурации зоны DNS, который будет установлен в группе зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="2081e-106">The **New-AzPrivateDnsZoneConfig** cmdlet enables you to create a new DNS zone configuration object which will be set on DNS zone group.</span></span>

## <span data-ttu-id="2081e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2081e-107">EXAMPLES</span></span>

### <span data-ttu-id="2081e-108">Создание конфигурации зоны DNS</span><span class="sxs-lookup"><span data-stu-id="2081e-108">Creates DNS zone configuration</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
```

<span data-ttu-id="2081e-109">В приведенном выше примере создается зона DNS, а затем создается конфигурация зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="2081e-109">The above example creates DNS zone and then creates DNS zone configuration.</span></span> <span data-ttu-id="2081e-110">`New-AzPrivateDnsZone` Командлет доявляется модулем AZ. PrivateDns.</span><span class="sxs-lookup"><span data-stu-id="2081e-110">`New-AzPrivateDnsZone` cmdlet is proveded by module Az.PrivateDns.</span></span>

## <span data-ttu-id="2081e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2081e-111">PARAMETERS</span></span>

### <span data-ttu-id="2081e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2081e-112">-DefaultProfile</span></span>
<span data-ttu-id="2081e-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2081e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2081e-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2081e-114">-Name</span></span>
<span data-ttu-id="2081e-115">Имя ресурса, уникального в рамках группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2081e-115">Name of the resource that is unique within a resource group.</span></span>
<span data-ttu-id="2081e-116">Это имя можно использовать для доступа к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="2081e-116">This name can be used to access the resource.</span></span>

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

### <span data-ttu-id="2081e-117">-PrivateDnsZoneId</span><span class="sxs-lookup"><span data-stu-id="2081e-117">-PrivateDnsZoneId</span></span>
<span data-ttu-id="2081e-118">Идентификатор ресурса частной зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="2081e-118">The resource id of the private dns zone.</span></span>

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

### <span data-ttu-id="2081e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2081e-119">CommonParameters</span></span>
<span data-ttu-id="2081e-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2081e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2081e-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2081e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2081e-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2081e-122">INPUTS</span></span>

### <span data-ttu-id="2081e-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="2081e-123">None</span></span>

## <span data-ttu-id="2081e-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2081e-124">OUTPUTS</span></span>

### <span data-ttu-id="2081e-125">Microsoft. Azure. Commands. Network. Models. PSPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="2081e-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="2081e-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="2081e-126">NOTES</span></span>

## <span data-ttu-id="2081e-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2081e-127">RELATED LINKS</span></span>
