---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
ms.openlocfilehash: 0f48bf7ad03dcfd59f8ea3653acdb7a57aa5240c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560172"
---
# <span data-ttu-id="1e127-101">Remove-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="1e127-101">Remove-AzureRmIotHubKey</span></span>

## <span data-ttu-id="1e127-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1e127-102">SYNOPSIS</span></span>
<span data-ttu-id="1e127-103">Удаление IotHubого ключа.</span><span class="sxs-lookup"><span data-stu-id="1e127-103">Removes an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e127-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1e127-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e127-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e127-105">DESCRIPTION</span></span>
<span data-ttu-id="1e127-106">Удаление IotHubого ключа.</span><span class="sxs-lookup"><span data-stu-id="1e127-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="1e127-107">Если в списке есть несколько клавиш с одинаковым именем, первый из них будет удален.</span><span class="sxs-lookup"><span data-stu-id="1e127-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="1e127-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1e127-108">EXAMPLES</span></span>

### <span data-ttu-id="1e127-109">Пример 1 удаление IotHub</span><span class="sxs-lookup"><span data-stu-id="1e127-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="1e127-110">Удаление ключа с именем iothubowner1 из IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="1e127-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="1e127-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1e127-111">PARAMETERS</span></span>

### <span data-ttu-id="1e127-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e127-112">-DefaultProfile</span></span>
<span data-ttu-id="1e127-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1e127-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e127-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="1e127-114">-KeyName</span></span>
<span data-ttu-id="1e127-115">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="1e127-115">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e127-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1e127-116">-Name</span></span>
<span data-ttu-id="1e127-117">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="1e127-117">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e127-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e127-118">-ResourceGroupName</span></span>
<span data-ttu-id="1e127-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1e127-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e127-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e127-120">-Confirm</span></span>
<span data-ttu-id="1e127-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1e127-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e127-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e127-122">-WhatIf</span></span>
<span data-ttu-id="1e127-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1e127-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e127-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1e127-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e127-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e127-125">CommonParameters</span></span>
<span data-ttu-id="1e127-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1e127-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e127-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e127-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e127-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1e127-128">INPUTS</span></span>

### <span data-ttu-id="1e127-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1e127-129">System.String</span></span>

## <span data-ttu-id="1e127-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e127-130">OUTPUTS</span></span>

### <span data-ttu-id="1e127-131">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1e127-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="1e127-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="1e127-132">NOTES</span></span>

## <span data-ttu-id="1e127-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e127-133">RELATED LINKS</span></span>
