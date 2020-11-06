---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 41F8F851-6F9F-4DA4-8CE6-D8C9B7CF68D7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementGateway.md
ms.openlocfilehash: 2bcfac139d38f0b6f7d621a7761ce01d1d3f2f45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565138"
---
# <span data-ttu-id="49333-101">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="49333-101">Remove-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="49333-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49333-102">SYNOPSIS</span></span>
<span data-ttu-id="49333-103">Удаляет шлюз управления сервером.</span><span class="sxs-lookup"><span data-stu-id="49333-103">Removes a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49333-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49333-104">SYNTAX</span></span>

### <span data-ttu-id="49333-105">ByName</span><span class="sxs-lookup"><span data-stu-id="49333-105">ByName</span></span>
```
Remove-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49333-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="49333-106">ByObject</span></span>
```
Remove-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49333-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49333-107">DESCRIPTION</span></span>
<span data-ttu-id="49333-108">Командлет **Remove-AzureRmServerManagementGateway** удаляет шлюз управления сервером Azure.</span><span class="sxs-lookup"><span data-stu-id="49333-108">The **Remove-AzureRmServerManagementGateway** cmdlet removes an Azure Server Management gateway.</span></span>

## <span data-ttu-id="49333-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49333-109">EXAMPLES</span></span>

## <span data-ttu-id="49333-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49333-110">PARAMETERS</span></span>

### <span data-ttu-id="49333-111">-Gateway</span><span class="sxs-lookup"><span data-stu-id="49333-111">-Gateway</span></span>
<span data-ttu-id="49333-112">Указывает шлюз, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="49333-112">Specifies the gateway that this cmdlet removes.</span></span>

<span data-ttu-id="49333-113">Этот параметр можно использовать вместо параметров *ResourceGroupName* и *GatewayName* .</span><span class="sxs-lookup"><span data-stu-id="49333-113">This parameter may be used instead of the *ResourceGroupName* and the *GatewayName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49333-114">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="49333-114">-GatewayName</span></span>
<span data-ttu-id="49333-115">Указывает имя шлюза, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="49333-115">Specifies the name of the gateway that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49333-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49333-116">-ResourceGroupName</span></span>
<span data-ttu-id="49333-117">Указывает имя группы ресурсов, к которой принадлежит шлюз.</span><span class="sxs-lookup"><span data-stu-id="49333-117">Specifies the name of the resource group in that the gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49333-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49333-118">-DefaultProfile</span></span>
<span data-ttu-id="49333-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49333-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49333-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49333-120">CommonParameters</span></span>
<span data-ttu-id="49333-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49333-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49333-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49333-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49333-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49333-123">INPUTS</span></span>

### <span data-ttu-id="49333-124">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="49333-124">Gateway</span></span>
<span data-ttu-id="49333-125">Параметр Gateway принимает от конвейера значение типа Gateway.</span><span class="sxs-lookup"><span data-stu-id="49333-125">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="49333-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49333-126">OUTPUTS</span></span>

## <span data-ttu-id="49333-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="49333-127">NOTES</span></span>
* <span data-ttu-id="49333-128">Прежде чем использовать этот командлет, необходимо удалить все узлы шлюза. в противном случае произойдет сбой командлета.</span><span class="sxs-lookup"><span data-stu-id="49333-128">All the nodes in the Gateway must be removed before using this cmdlet; otherwise this cmdlet will fail.</span></span>

## <span data-ttu-id="49333-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49333-129">RELATED LINKS</span></span>

[<span data-ttu-id="49333-130">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="49333-130">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="49333-131">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="49333-131">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)


