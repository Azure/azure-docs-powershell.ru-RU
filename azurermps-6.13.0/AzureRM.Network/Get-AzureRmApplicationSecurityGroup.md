---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 49c7a9a28da7822423e43ee655b1ff2256e957e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733446"
---
# <span data-ttu-id="6c98a-101">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6c98a-101">Get-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="6c98a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6c98a-102">SYNOPSIS</span></span>
<span data-ttu-id="6c98a-103">Получает группу безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="6c98a-103">Gets an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c98a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6c98a-104">SYNTAX</span></span>

```
Get-AzureRmApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c98a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c98a-105">DESCRIPTION</span></span>
<span data-ttu-id="6c98a-106">Командлет **Get-AzureRmApplicationSecurityGroup** получает группу безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="6c98a-106">The **Get-AzureRmApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="6c98a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6c98a-107">EXAMPLES</span></span>

### <span data-ttu-id="6c98a-108">Пример 1: получение всех групп безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="6c98a-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup
```

<span data-ttu-id="6c98a-109">В приведенной выше команде возвращаются все группы безопасности приложений в подписке.</span><span class="sxs-lookup"><span data-stu-id="6c98a-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="6c98a-110">Пример 2: получение групп безопасности приложений в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6c98a-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="6c98a-111">В приведенной выше команде возвращаются все группы безопасности приложения, которые принадлежат группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6c98a-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="6c98a-112">Пример 3: получение определенной группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="6c98a-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

<span data-ttu-id="6c98a-113">Приведенная выше команда возвращает группу безопасности приложения MyApplicationSecurityGroup в группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6c98a-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

## <span data-ttu-id="6c98a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6c98a-114">PARAMETERS</span></span>

### <span data-ttu-id="6c98a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c98a-115">-DefaultProfile</span></span>
<span data-ttu-id="6c98a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6c98a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c98a-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6c98a-117">-Name</span></span>
<span data-ttu-id="6c98a-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="6c98a-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c98a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c98a-119">-ResourceGroupName</span></span>
<span data-ttu-id="6c98a-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6c98a-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c98a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c98a-121">CommonParameters</span></span>
<span data-ttu-id="6c98a-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6c98a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c98a-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c98a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c98a-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6c98a-124">INPUTS</span></span>

### <span data-ttu-id="6c98a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6c98a-125">System.String</span></span>

## <span data-ttu-id="6c98a-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c98a-126">OUTPUTS</span></span>

### <span data-ttu-id="6c98a-127">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6c98a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="6c98a-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="6c98a-128">NOTES</span></span>

## <span data-ttu-id="6c98a-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c98a-129">RELATED LINKS</span></span>

[<span data-ttu-id="6c98a-130">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6c98a-130">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="6c98a-131">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6c98a-131">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="6c98a-132">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6c98a-132">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="6c98a-133">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6c98a-133">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)
