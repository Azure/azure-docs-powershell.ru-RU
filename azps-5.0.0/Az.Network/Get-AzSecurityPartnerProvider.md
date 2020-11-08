---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
ms.openlocfilehash: 8dd23c7eba3dd9306527c11afe5170740a464d2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249690"
---
# <span data-ttu-id="f95b5-101">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f95b5-101">Get-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="f95b5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f95b5-102">SYNOPSIS</span></span>
<span data-ttu-id="f95b5-103">Получить Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f95b5-103">Get an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="f95b5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f95b5-104">SYNTAX</span></span>

### <span data-ttu-id="f95b5-105">SecurityPartnerProviderNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f95b5-105">SecurityPartnerProviderNameParameterSet (Default)</span></span>
```
Get-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f95b5-106">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f95b5-106">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Get-AzSecurityPartnerProvider -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f95b5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f95b5-107">DESCRIPTION</span></span>
<span data-ttu-id="f95b5-108">Командлет **Get-AzSecurityPartnerProvider** получает Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f95b5-108">The **Get-AzSecurityPartnerProvider** cmdlet gets an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="f95b5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f95b5-109">EXAMPLES</span></span>

### <span data-ttu-id="f95b5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f95b5-110">Example 1</span></span>
```powershell
Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```


### <span data-ttu-id="f95b5-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f95b5-111">Example 2</span></span>
```powershell
$securityPartnerProviderId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/securityPartnerProviderRG/providers/Microsoft.Network/securityPartnerProvider/securityPartnerProvider'
Get-AzSecurityPartnerProvider -ResourceId $securityPartnerProviderId
```

## <span data-ttu-id="f95b5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f95b5-112">PARAMETERS</span></span>

### <span data-ttu-id="f95b5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f95b5-113">-DefaultProfile</span></span>
<span data-ttu-id="f95b5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f95b5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f95b5-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f95b5-115">-Name</span></span>
<span data-ttu-id="f95b5-116">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="f95b5-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f95b5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f95b5-117">-ResourceGroupName</span></span>
<span data-ttu-id="f95b5-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f95b5-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f95b5-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f95b5-119">-ResourceId</span></span>
<span data-ttu-id="f95b5-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="f95b5-120">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f95b5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f95b5-121">CommonParameters</span></span>
<span data-ttu-id="f95b5-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f95b5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f95b5-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f95b5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f95b5-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f95b5-124">INPUTS</span></span>

### <span data-ttu-id="f95b5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f95b5-125">System.String</span></span>

## <span data-ttu-id="f95b5-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f95b5-126">OUTPUTS</span></span>

### <span data-ttu-id="f95b5-127">Microsoft. Azure. Commands. Network. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f95b5-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="f95b5-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="f95b5-128">NOTES</span></span>

## <span data-ttu-id="f95b5-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f95b5-129">RELATED LINKS</span></span>
