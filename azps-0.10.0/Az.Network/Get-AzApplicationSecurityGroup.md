---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: b23901a79262f4eb63e34b99c10b82442cb2fe6a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910033"
---
# <span data-ttu-id="59c98-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="59c98-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="59c98-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59c98-102">SYNOPSIS</span></span>
<span data-ttu-id="59c98-103">Получает группу безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="59c98-103">Gets an application security group.</span></span>

## <span data-ttu-id="59c98-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59c98-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59c98-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59c98-105">DESCRIPTION</span></span>
<span data-ttu-id="59c98-106">Командлет **Get-AzApplicationSecurityGroup** получает группу безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="59c98-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="59c98-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59c98-107">EXAMPLES</span></span>

### <span data-ttu-id="59c98-108">Пример 1: получение всех групп безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="59c98-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup
```

<span data-ttu-id="59c98-109">В приведенной выше команде возвращаются все группы безопасности приложений в подписке.</span><span class="sxs-lookup"><span data-stu-id="59c98-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="59c98-110">Пример 2: получение групп безопасности приложений в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="59c98-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="59c98-111">В приведенной выше команде возвращаются все группы безопасности приложения, которые принадлежат группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="59c98-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="59c98-112">Пример 3: получение определенной группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="59c98-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

<span data-ttu-id="59c98-113">Приведенная выше команда возвращает группу безопасности приложения MyApplicationSecurityGroup в группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="59c98-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

## <span data-ttu-id="59c98-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59c98-114">PARAMETERS</span></span>

### <span data-ttu-id="59c98-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59c98-115">-DefaultProfile</span></span>
<span data-ttu-id="59c98-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59c98-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59c98-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="59c98-117">-Name</span></span>
<span data-ttu-id="59c98-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="59c98-118">The resource name.</span></span>

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

### <span data-ttu-id="59c98-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59c98-119">-ResourceGroupName</span></span>
<span data-ttu-id="59c98-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="59c98-120">The resource group name.</span></span>

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

### <span data-ttu-id="59c98-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59c98-121">CommonParameters</span></span>
<span data-ttu-id="59c98-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59c98-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59c98-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59c98-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59c98-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59c98-124">INPUTS</span></span>

### <span data-ttu-id="59c98-125">System. String</span><span class="sxs-lookup"><span data-stu-id="59c98-125">System.String</span></span>

## <span data-ttu-id="59c98-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59c98-126">OUTPUTS</span></span>

### <span data-ttu-id="59c98-127">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="59c98-127">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="59c98-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="59c98-128">NOTES</span></span>

## <span data-ttu-id="59c98-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59c98-129">RELATED LINKS</span></span>

[<span data-ttu-id="59c98-130">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="59c98-130">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="59c98-131">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="59c98-131">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="59c98-132">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59c98-132">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="59c98-133">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="59c98-133">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)
