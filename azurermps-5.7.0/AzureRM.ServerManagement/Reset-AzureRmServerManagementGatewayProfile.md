---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 22B63259-799B-4F25-A06B-7A818D295870
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/reset-azurermservermanagementgatewayprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: 0833266bcd6e98a1d9744db2bc202bce5a01f3f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561499"
---
# <span data-ttu-id="09b50-101">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="09b50-101">Reset-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="09b50-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="09b50-102">SYNOPSIS</span></span>
<span data-ttu-id="09b50-103">Сброс профиля шлюза управления сервером.</span><span class="sxs-lookup"><span data-stu-id="09b50-103">Resets the profile of a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09b50-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="09b50-104">SYNTAX</span></span>

### <span data-ttu-id="09b50-105">ByName</span><span class="sxs-lookup"><span data-stu-id="09b50-105">ByName</span></span>
```
Reset-AzureRmServerManagementGatewayProfile [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09b50-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="09b50-106">ByObject</span></span>
```
Reset-AzureRmServerManagementGatewayProfile [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="09b50-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09b50-107">DESCRIPTION</span></span>
<span data-ttu-id="09b50-108">Командлет **Reset-AzureRmServerManagementGatewayProfile** сбрасывает профиль шлюза управления сервером Azure Server.</span><span class="sxs-lookup"><span data-stu-id="09b50-108">The **Reset-AzureRmServerManagementGatewayProfile** cmdlet resets the profile for an Azure Server Management Gateway.</span></span>

<span data-ttu-id="09b50-109">Вам потребуется использовать командлет Save-AzureRmServerManagementGatewayProfile для загрузки профиля, а затем командлет Install-AzureRmServerManagementGatewayProfile, чтобы сохранить его после сброса профиля.</span><span class="sxs-lookup"><span data-stu-id="09b50-109">You will need to use the Save-AzureRmServerManagementGatewayProfile cmdlet to download the profile and then the Install-AzureRmServerManagementGatewayProfile cmdlet to save it after you reset the profile.</span></span>

## <span data-ttu-id="09b50-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="09b50-110">EXAMPLES</span></span>

## <span data-ttu-id="09b50-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="09b50-111">PARAMETERS</span></span>

### <span data-ttu-id="09b50-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09b50-112">-DefaultProfile</span></span>
<span data-ttu-id="09b50-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="09b50-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09b50-114">-Gateway</span><span class="sxs-lookup"><span data-stu-id="09b50-114">-Gateway</span></span>
<span data-ttu-id="09b50-115">Указывает шлюз, для которого командлет сбрасывает профиль.</span><span class="sxs-lookup"><span data-stu-id="09b50-115">Specifies the gateway for which the cmdlet resets the profile for.</span></span>

<span data-ttu-id="09b50-116">Может быть указан вместо ResourceGoupName и GatewayName</span><span class="sxs-lookup"><span data-stu-id="09b50-116">May be specified instead of ResourceGoupName and GatewayName</span></span>

```yaml
Type: Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09b50-117">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="09b50-117">-GatewayName</span></span>
<span data-ttu-id="09b50-118">Указывает имя шлюза, для которого командлет сбрасывает профиль.</span><span class="sxs-lookup"><span data-stu-id="09b50-118">Specifies the name of the gateway for which the cmdlet resets the profile.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09b50-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09b50-119">-ResourceGroupName</span></span>
<span data-ttu-id="09b50-120">Указывает имя группы ресурсов, к которой принадлежит шлюз.</span><span class="sxs-lookup"><span data-stu-id="09b50-120">Specifies the name of the resource group that the gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09b50-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09b50-121">CommonParameters</span></span>
<span data-ttu-id="09b50-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="09b50-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09b50-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09b50-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09b50-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="09b50-124">INPUTS</span></span>

### <span data-ttu-id="09b50-125">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="09b50-125">Gateway</span></span>
<span data-ttu-id="09b50-126">Параметр Gateway принимает от конвейера значение типа Gateway.</span><span class="sxs-lookup"><span data-stu-id="09b50-126">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="09b50-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="09b50-127">OUTPUTS</span></span>

## <span data-ttu-id="09b50-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="09b50-128">NOTES</span></span>

## <span data-ttu-id="09b50-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09b50-129">RELATED LINKS</span></span>

[<span data-ttu-id="09b50-130">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="09b50-130">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="09b50-131">Сохранить — AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="09b50-131">Save-AzureRmServerManagementGatewayProfile</span></span>](./Save-AzureRmServerManagementGatewayProfile.md)


