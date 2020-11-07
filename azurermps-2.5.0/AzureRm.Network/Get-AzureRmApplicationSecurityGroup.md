---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationsecuritygroup
schema: 2.0.0
ms.openlocfilehash: 52050426c34b30bcab867643fbb3e5b9c373f3f2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913457"
---
# <span data-ttu-id="51fa4-101">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="51fa4-101">Get-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="51fa4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51fa4-102">SYNOPSIS</span></span>
<span data-ttu-id="51fa4-103">Получает группу безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="51fa4-103">Gets an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51fa4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51fa4-104">SYNTAX</span></span>

```
Get-AzureRmApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51fa4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51fa4-105">DESCRIPTION</span></span>
<span data-ttu-id="51fa4-106">Командлет **Get-AzureRmApplicationSecurityGroup** получает группу безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="51fa4-106">The **Get-AzureRmApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="51fa4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51fa4-107">EXAMPLES</span></span>

### <span data-ttu-id="51fa4-108">Пример 1: получение всех групп безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="51fa4-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup
```

<span data-ttu-id="51fa4-109">В приведенной выше команде возвращаются все группы безопасности приложений в подписке.</span><span class="sxs-lookup"><span data-stu-id="51fa4-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="51fa4-110">Пример 2: получение групп безопасности приложений в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="51fa4-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="51fa4-111">В приведенной выше команде возвращаются все группы безопасности приложения, которые принадлежат группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="51fa4-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="51fa4-112">Пример 3: получение определенной группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="51fa4-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

<span data-ttu-id="51fa4-113">Приведенная выше команда возвращает группу безопасности приложения MyApplicationSecurityGroup в группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="51fa4-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

## <span data-ttu-id="51fa4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51fa4-114">PARAMETERS</span></span>

### <span data-ttu-id="51fa4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51fa4-115">-DefaultProfile</span></span>
<span data-ttu-id="51fa4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="51fa4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51fa4-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="51fa4-117">-Name</span></span>
<span data-ttu-id="51fa4-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="51fa4-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51fa4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51fa4-119">-ResourceGroupName</span></span>
<span data-ttu-id="51fa4-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="51fa4-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51fa4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51fa4-121">CommonParameters</span></span>
<span data-ttu-id="51fa4-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51fa4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51fa4-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51fa4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51fa4-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51fa4-124">INPUTS</span></span>

### <span data-ttu-id="51fa4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="51fa4-125">System.String</span></span>

## <span data-ttu-id="51fa4-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51fa4-126">OUTPUTS</span></span>

### <span data-ttu-id="51fa4-127">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="51fa4-127">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="51fa4-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="51fa4-128">NOTES</span></span>

## <span data-ttu-id="51fa4-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51fa4-129">RELATED LINKS</span></span>

[<span data-ttu-id="51fa4-130">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="51fa4-130">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="51fa4-131">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="51fa4-131">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="51fa4-132">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="51fa4-132">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="51fa4-133">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="51fa4-133">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)
