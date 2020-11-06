---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 704c4c2a11cc83136481573190e745d7a4b2c83f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569331"
---
# <span data-ttu-id="468f9-101">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="468f9-101">Get-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="468f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="468f9-102">SYNOPSIS</span></span>
<span data-ttu-id="468f9-103">Получает группу безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="468f9-103">Gets an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="468f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="468f9-104">SYNTAX</span></span>

```
Get-AzureRmApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="468f9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="468f9-105">DESCRIPTION</span></span>
<span data-ttu-id="468f9-106">Командлет **Get-AzureRmApplicationSecurityGroup** получает группу безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="468f9-106">The **Get-AzureRmApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="468f9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="468f9-107">EXAMPLES</span></span>

### <span data-ttu-id="468f9-108">Пример 1: получение всех групп безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="468f9-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup
```

<span data-ttu-id="468f9-109">В приведенной выше команде возвращаются все группы безопасности приложений в подписке.</span><span class="sxs-lookup"><span data-stu-id="468f9-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="468f9-110">Пример 2: получение групп безопасности приложений в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="468f9-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="468f9-111">В приведенной выше команде возвращаются все группы безопасности приложения, которые принадлежат группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="468f9-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="468f9-112">Пример 3: получение определенной группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="468f9-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

<span data-ttu-id="468f9-113">Приведенная выше команда возвращает группу безопасности приложения MyApplicationSecurityGroup в группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="468f9-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

## <span data-ttu-id="468f9-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="468f9-114">PARAMETERS</span></span>

### <span data-ttu-id="468f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="468f9-115">-DefaultProfile</span></span>
<span data-ttu-id="468f9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="468f9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="468f9-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="468f9-117">-Name</span></span>
<span data-ttu-id="468f9-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="468f9-118">The resource name.</span></span>

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

### <span data-ttu-id="468f9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="468f9-119">-ResourceGroupName</span></span>
<span data-ttu-id="468f9-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="468f9-120">The resource group name.</span></span>

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

### <span data-ttu-id="468f9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="468f9-121">CommonParameters</span></span>
<span data-ttu-id="468f9-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="468f9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="468f9-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="468f9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="468f9-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="468f9-124">INPUTS</span></span>

### <span data-ttu-id="468f9-125">System. String</span><span class="sxs-lookup"><span data-stu-id="468f9-125">System.String</span></span>

## <span data-ttu-id="468f9-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="468f9-126">OUTPUTS</span></span>

### <span data-ttu-id="468f9-127">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="468f9-127">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="468f9-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="468f9-128">NOTES</span></span>

## <span data-ttu-id="468f9-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="468f9-129">RELATED LINKS</span></span>

[<span data-ttu-id="468f9-130">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="468f9-130">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="468f9-131">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="468f9-131">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="468f9-132">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="468f9-132">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="468f9-133">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="468f9-133">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)
