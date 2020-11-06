---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
ms.openlocfilehash: f7bbe0c37d03a6db372c6c70da021160060a542a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567621"
---
# <span data-ttu-id="c9836-101">Add-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="c9836-101">Add-AzureRmIotHubKey</span></span>

## <span data-ttu-id="c9836-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c9836-102">SYNOPSIS</span></span>
<span data-ttu-id="c9836-103">Создание ключа IotHub.</span><span class="sxs-lookup"><span data-stu-id="c9836-103">Creates an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9836-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c9836-104">SYNTAX</span></span>

```
Add-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [[-PrimaryKey] <String>] [[-SecondaryKey] <String>] [-Rights] <PSAccessRights>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9836-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9836-105">DESCRIPTION</span></span>
<span data-ttu-id="c9836-106">Создает ключ для указанного IotHub.</span><span class="sxs-lookup"><span data-stu-id="c9836-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="c9836-107">KeyNames не являются уникальными и нуждаются в тщательном управлении.</span><span class="sxs-lookup"><span data-stu-id="c9836-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="c9836-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c9836-108">EXAMPLES</span></span>

### <span data-ttu-id="c9836-109">Пример 1. Добавление ключа в IotHub</span><span class="sxs-lookup"><span data-stu-id="c9836-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="c9836-110">Создает ключ с именем "myKey" для iothub "myiothub" с разрешениями RegistryRead.</span><span class="sxs-lookup"><span data-stu-id="c9836-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="c9836-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c9836-111">PARAMETERS</span></span>

### <span data-ttu-id="c9836-112">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c9836-112">-KeyName</span></span>
<span data-ttu-id="c9836-113">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="c9836-113">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9836-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c9836-114">-Name</span></span>
<span data-ttu-id="c9836-115">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="c9836-115">Name of the IotHub</span></span>

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

### <span data-ttu-id="c9836-116">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="c9836-116">-PrimaryKey</span></span>
<span data-ttu-id="c9836-117">Первичный ключ</span><span class="sxs-lookup"><span data-stu-id="c9836-117">The primary key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9836-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9836-118">-ResourceGroupName</span></span>
<span data-ttu-id="c9836-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c9836-119">Resource Group Name</span></span>

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

### <span data-ttu-id="c9836-120">-Права</span><span class="sxs-lookup"><span data-stu-id="c9836-120">-Rights</span></span>
<span data-ttu-id="c9836-121">Разрешения для этого IOTHub</span><span class="sxs-lookup"><span data-stu-id="c9836-121">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases: 
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9836-122">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="c9836-122">-SecondaryKey</span></span>
<span data-ttu-id="c9836-123">Вторичный ключ</span><span class="sxs-lookup"><span data-stu-id="c9836-123">The Secondary Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9836-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9836-124">-Confirm</span></span>
<span data-ttu-id="c9836-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c9836-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9836-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9836-126">-WhatIf</span></span>
<span data-ttu-id="c9836-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c9836-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9836-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c9836-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9836-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9836-129">-DefaultProfile</span></span>
<span data-ttu-id="c9836-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c9836-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9836-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9836-131">CommonParameters</span></span>
<span data-ttu-id="c9836-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c9836-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9836-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9836-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9836-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c9836-134">INPUTS</span></span>

### <span data-ttu-id="c9836-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c9836-135">System.String</span></span>
<span data-ttu-id="c9836-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSAccessRights</span><span class="sxs-lookup"><span data-stu-id="c9836-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights</span></span>

## <span data-ttu-id="c9836-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9836-137">OUTPUTS</span></span>

### <span data-ttu-id="c9836-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c9836-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="c9836-139">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="c9836-139">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="c9836-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="c9836-140">NOTES</span></span>

## <span data-ttu-id="c9836-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9836-141">RELATED LINKS</span></span>

