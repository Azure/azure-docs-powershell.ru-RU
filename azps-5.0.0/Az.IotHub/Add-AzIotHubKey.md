---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: 422eb25456beb57ed6ab029fa5d70a47061ca491
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247778"
---
# <span data-ttu-id="b8a2c-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="b8a2c-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="b8a2c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8a2c-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a2c-103">Создание ключа IotHub.</span><span class="sxs-lookup"><span data-stu-id="b8a2c-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="b8a2c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8a2c-104">SYNTAX</span></span>

### <span data-ttu-id="b8a2c-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b8a2c-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8a2c-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b8a2c-106">ResourceIdSet</span></span>
```
Add-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8a2c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8a2c-107">DESCRIPTION</span></span>
<span data-ttu-id="b8a2c-108">Создает ключ для указанного IotHub.</span><span class="sxs-lookup"><span data-stu-id="b8a2c-108">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="b8a2c-109">KeyNames не являются уникальными и нуждаются в тщательном управлении.</span><span class="sxs-lookup"><span data-stu-id="b8a2c-109">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="b8a2c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8a2c-110">EXAMPLES</span></span>

### <span data-ttu-id="b8a2c-111">Пример 1. Добавление ключа в IotHub</span><span class="sxs-lookup"><span data-stu-id="b8a2c-111">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="b8a2c-112">Создает ключ с именем "myKey" для iothub "myiothub" с разрешениями RegistryRead.</span><span class="sxs-lookup"><span data-stu-id="b8a2c-112">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="b8a2c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8a2c-113">PARAMETERS</span></span>

### <span data-ttu-id="b8a2c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a2c-114">-DefaultProfile</span></span>
<span data-ttu-id="b8a2c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b8a2c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a2c-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="b8a2c-116">-HubId</span></span>
<span data-ttu-id="b8a2c-117">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="b8a2c-117">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a2c-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="b8a2c-118">-KeyName</span></span>
<span data-ttu-id="b8a2c-119">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="b8a2c-119">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a2c-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b8a2c-120">-Name</span></span>
<span data-ttu-id="b8a2c-121">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="b8a2c-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a2c-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="b8a2c-122">-PrimaryKey</span></span>
<span data-ttu-id="b8a2c-123">Первичный ключ</span><span class="sxs-lookup"><span data-stu-id="b8a2c-123">The primary key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a2c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8a2c-124">-ResourceGroupName</span></span>
<span data-ttu-id="b8a2c-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b8a2c-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a2c-126">-Права</span><span class="sxs-lookup"><span data-stu-id="b8a2c-126">-Rights</span></span>
<span data-ttu-id="b8a2c-127">Разрешения для этого IOTHub</span><span class="sxs-lookup"><span data-stu-id="b8a2c-127">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases:
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a2c-128">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="b8a2c-128">-SecondaryKey</span></span>
<span data-ttu-id="b8a2c-129">Вторичный ключ</span><span class="sxs-lookup"><span data-stu-id="b8a2c-129">The Secondary Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a2c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8a2c-130">-Confirm</span></span>
<span data-ttu-id="b8a2c-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b8a2c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8a2c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8a2c-132">-WhatIf</span></span>
<span data-ttu-id="b8a2c-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b8a2c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8a2c-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b8a2c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8a2c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a2c-135">CommonParameters</span></span>
<span data-ttu-id="b8a2c-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8a2c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a2c-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8a2c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a2c-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8a2c-138">INPUTS</span></span>

### <span data-ttu-id="b8a2c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b8a2c-139">System.String</span></span>

## <span data-ttu-id="b8a2c-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8a2c-140">OUTPUTS</span></span>

### <span data-ttu-id="b8a2c-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b8a2c-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="b8a2c-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8a2c-142">NOTES</span></span>

## <span data-ttu-id="b8a2c-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8a2c-143">RELATED LINKS</span></span>
