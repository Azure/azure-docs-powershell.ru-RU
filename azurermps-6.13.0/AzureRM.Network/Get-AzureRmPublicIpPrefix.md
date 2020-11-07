---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpPrefix.md
ms.openlocfilehash: 772f0a3bb1198bf5c8d00ad8c0dd708c37c92366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732472"
---
# <span data-ttu-id="cb4c9-101">Get-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cb4c9-101">Get-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="cb4c9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cb4c9-102">SYNOPSIS</span></span>
<span data-ttu-id="cb4c9-103">Получает префикс общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="cb4c9-103">Gets a public IP prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb4c9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cb4c9-104">SYNTAX</span></span>

### <span data-ttu-id="cb4c9-105">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="cb4c9-105">(Default)</span></span>
```
Get-AzureRmPublicIpPrefix [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb4c9-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb4c9-106">GetByNameParameterSet</span></span>
```
Get-AzureRmPublicIpPrefix [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb4c9-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb4c9-107">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb4c9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb4c9-108">DESCRIPTION</span></span>
<span data-ttu-id="cb4c9-109">Командлет **Get-AzureRmPublicIpPrefix** получает один или несколько общедоступных префиксов IP-адресов в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb4c9-109">The **Get-AzureRmPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="cb4c9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cb4c9-110">EXAMPLES</span></span>

### <span data-ttu-id="cb4c9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cb4c9-111">Example 1</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzureRmPublicIpPrefix -ResourceGroupName $rgname -Name $prefixName
```

<span data-ttu-id="cb4c9-112">Эта команда получает ресурс префикса общедоступного IP-адреса с $prefixName в группе ресурсов $rgName</span><span class="sxs-lookup"><span data-stu-id="cb4c9-112">This command gets a public IP prefix resource with $prefixName in resource group $rgName</span></span>

## <span data-ttu-id="cb4c9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cb4c9-113">PARAMETERS</span></span>

### <span data-ttu-id="cb4c9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb4c9-114">-DefaultProfile</span></span>
<span data-ttu-id="cb4c9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb4c9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb4c9-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cb4c9-116">-Name</span></span>
<span data-ttu-id="cb4c9-117">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb4c9-117">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb4c9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb4c9-118">-ResourceGroupName</span></span>
<span data-ttu-id="cb4c9-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb4c9-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb4c9-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb4c9-120">-ResourceId</span></span>
<span data-ttu-id="cb4c9-121">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb4c9-121">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb4c9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb4c9-122">CommonParameters</span></span>
<span data-ttu-id="cb4c9-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cb4c9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cb4c9-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb4c9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb4c9-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cb4c9-125">INPUTS</span></span>

### <span data-ttu-id="cb4c9-126">System. String</span><span class="sxs-lookup"><span data-stu-id="cb4c9-126">System.String</span></span>


## <span data-ttu-id="cb4c9-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb4c9-127">OUTPUTS</span></span>

### <span data-ttu-id="cb4c9-128">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cb4c9-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="cb4c9-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="cb4c9-129">NOTES</span></span>

## <span data-ttu-id="cb4c9-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb4c9-130">RELATED LINKS</span></span>
