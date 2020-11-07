---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 22B63259-799B-4F25-A06B-7A818D295870
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: 9ce8dc1faf1a762a847da5eb87fb28b510308054
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733318"
---
# <span data-ttu-id="86fda-101">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="86fda-101">Reset-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="86fda-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="86fda-102">SYNOPSIS</span></span>
<span data-ttu-id="86fda-103">Сброс профиля шлюза управления сервером.</span><span class="sxs-lookup"><span data-stu-id="86fda-103">Resets the profile of a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86fda-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="86fda-104">SYNTAX</span></span>

### <span data-ttu-id="86fda-105">ByName</span><span class="sxs-lookup"><span data-stu-id="86fda-105">ByName</span></span>
```
Reset-AzureRmServerManagementGatewayProfile [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86fda-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="86fda-106">ByObject</span></span>
```
Reset-AzureRmServerManagementGatewayProfile [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="86fda-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86fda-107">DESCRIPTION</span></span>
<span data-ttu-id="86fda-108">Командлет **Reset-AzureRmServerManagementGatewayProfile** сбрасывает профиль шлюза управления сервером Azure Server.</span><span class="sxs-lookup"><span data-stu-id="86fda-108">The **Reset-AzureRmServerManagementGatewayProfile** cmdlet resets the profile for an Azure Server Management Gateway.</span></span>

<span data-ttu-id="86fda-109">Вам потребуется использовать командлет Save-AzureRmServerManagementGatewayProfile для загрузки профиля, а затем командлет Install-AzureRmServerManagementGatewayProfile, чтобы сохранить его после сброса профиля.</span><span class="sxs-lookup"><span data-stu-id="86fda-109">You will need to use the Save-AzureRmServerManagementGatewayProfile cmdlet to download the profile and then the Install-AzureRmServerManagementGatewayProfile cmdlet to save it after you reset the profile.</span></span>

## <span data-ttu-id="86fda-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="86fda-110">EXAMPLES</span></span>

## <span data-ttu-id="86fda-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="86fda-111">PARAMETERS</span></span>

### <span data-ttu-id="86fda-112">-Gateway</span><span class="sxs-lookup"><span data-stu-id="86fda-112">-Gateway</span></span>
<span data-ttu-id="86fda-113">Указывает шлюз, для которого командлет сбрасывает профиль.</span><span class="sxs-lookup"><span data-stu-id="86fda-113">Specifies the gateway for which the cmdlet resets the profile for.</span></span>

<span data-ttu-id="86fda-114">Может быть указан вместо ResourceGoupName и GatewayName</span><span class="sxs-lookup"><span data-stu-id="86fda-114">May be specified instead of ResourceGoupName and GatewayName</span></span>

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

### <span data-ttu-id="86fda-115">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="86fda-115">-GatewayName</span></span>
<span data-ttu-id="86fda-116">Указывает имя шлюза, для которого командлет сбрасывает профиль.</span><span class="sxs-lookup"><span data-stu-id="86fda-116">Specifies the name of the gateway for which the cmdlet resets the profile.</span></span>

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

### <span data-ttu-id="86fda-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86fda-117">-ResourceGroupName</span></span>
<span data-ttu-id="86fda-118">Указывает имя группы ресурсов, к которой принадлежит шлюз.</span><span class="sxs-lookup"><span data-stu-id="86fda-118">Specifies the name of the resource group that the gateway belongs to.</span></span>

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

### <span data-ttu-id="86fda-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86fda-119">-DefaultProfile</span></span>
<span data-ttu-id="86fda-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="86fda-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86fda-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86fda-121">CommonParameters</span></span>
<span data-ttu-id="86fda-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="86fda-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86fda-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86fda-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86fda-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="86fda-124">INPUTS</span></span>

### <span data-ttu-id="86fda-125">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="86fda-125">Gateway</span></span>
<span data-ttu-id="86fda-126">Параметр Gateway принимает от конвейера значение типа Gateway.</span><span class="sxs-lookup"><span data-stu-id="86fda-126">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="86fda-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="86fda-127">OUTPUTS</span></span>

## <span data-ttu-id="86fda-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="86fda-128">NOTES</span></span>

## <span data-ttu-id="86fda-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86fda-129">RELATED LINKS</span></span>

[<span data-ttu-id="86fda-130">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="86fda-130">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="86fda-131">Сохранить — AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="86fda-131">Save-AzureRmServerManagementGatewayProfile</span></span>](./Save-AzureRmServerManagementGatewayProfile.md)


