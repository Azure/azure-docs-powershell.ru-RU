---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 98adc5714f4a4abaeca9fe6723b1a56fe1d49fca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733804"
---
# <span data-ttu-id="ac9b6-101">Get-AzureRmSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="ac9b6-101">Get-AzureRmSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="ac9b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac9b6-102">SYNOPSIS</span></span>
<span data-ttu-id="ac9b6-103">Получает параметры автоматического обеспечения безопасности</span><span class="sxs-lookup"><span data-stu-id="ac9b6-103">Gets the security automatic provisioning settings</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac9b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac9b6-104">SYNTAX</span></span>

### <span data-ttu-id="ac9b6-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ac9b6-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac9b6-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="ac9b6-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac9b6-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac9b6-107">ResourceId</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac9b6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac9b6-108">DESCRIPTION</span></span>
<span data-ttu-id="ac9b6-109">Параметры автоматической подготовки позволяют решить, хотите ли вы, чтобы Azure Security Cetner автоматически proviosion агентом безопасности, который будет установлен на своих виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="ac9b6-109">Automatic Provisioning Settings let you decide whether you want Azure Security Cetner to automatically proviosion a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="ac9b6-110">Агент безопасности будет наблюдать за виртуальной машиной для создания оповещений системы безопасности и отслеживания соответствия требованиям безопасности виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ac9b6-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="ac9b6-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac9b6-111">EXAMPLES</span></span>

### <span data-ttu-id="ac9b6-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ac9b6-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="ac9b6-113">Получает параметр автоматической подготовки для подписки.</span><span class="sxs-lookup"><span data-stu-id="ac9b6-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="ac9b6-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac9b6-114">PARAMETERS</span></span>

### <span data-ttu-id="ac9b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac9b6-115">-DefaultProfile</span></span>
<span data-ttu-id="ac9b6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac9b6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac9b6-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ac9b6-117">-Name</span></span>
<span data-ttu-id="ac9b6-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="ac9b6-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac9b6-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac9b6-119">-ResourceId</span></span>
<span data-ttu-id="ac9b6-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="ac9b6-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac9b6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac9b6-121">CommonParameters</span></span>
<span data-ttu-id="ac9b6-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac9b6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac9b6-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac9b6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac9b6-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac9b6-124">INPUTS</span></span>

### <span data-ttu-id="ac9b6-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ac9b6-125">System.String</span></span>

## <span data-ttu-id="ac9b6-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac9b6-126">OUTPUTS</span></span>

### <span data-ttu-id="ac9b6-127">Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="ac9b6-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="ac9b6-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac9b6-128">NOTES</span></span>

## <span data-ttu-id="ac9b6-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac9b6-129">RELATED LINKS</span></span>
