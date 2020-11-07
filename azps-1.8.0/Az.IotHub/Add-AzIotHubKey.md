---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: f73cfd1cadff449289bfa82ab1de04d110fb0f1a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900390"
---
# <span data-ttu-id="0cf83-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="0cf83-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="0cf83-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0cf83-102">SYNOPSIS</span></span>
<span data-ttu-id="0cf83-103">Создание ключа IotHub.</span><span class="sxs-lookup"><span data-stu-id="0cf83-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="0cf83-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0cf83-104">SYNTAX</span></span>

```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cf83-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0cf83-105">DESCRIPTION</span></span>
<span data-ttu-id="0cf83-106">Создает ключ для указанного IotHub.</span><span class="sxs-lookup"><span data-stu-id="0cf83-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="0cf83-107">KeyNames не являются уникальными и нуждаются в тщательном управлении.</span><span class="sxs-lookup"><span data-stu-id="0cf83-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="0cf83-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0cf83-108">EXAMPLES</span></span>

### <span data-ttu-id="0cf83-109">Пример 1. Добавление ключа в IotHub</span><span class="sxs-lookup"><span data-stu-id="0cf83-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="0cf83-110">Создает ключ с именем "myKey" для iothub "myiothub" с разрешениями RegistryRead.</span><span class="sxs-lookup"><span data-stu-id="0cf83-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="0cf83-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0cf83-111">PARAMETERS</span></span>

### <span data-ttu-id="0cf83-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cf83-112">-DefaultProfile</span></span>
<span data-ttu-id="0cf83-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0cf83-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0cf83-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="0cf83-114">-KeyName</span></span>
<span data-ttu-id="0cf83-115">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="0cf83-115">Name of the Key</span></span>

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

### <span data-ttu-id="0cf83-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0cf83-116">-Name</span></span>
<span data-ttu-id="0cf83-117">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="0cf83-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="0cf83-118">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="0cf83-118">-PrimaryKey</span></span>
<span data-ttu-id="0cf83-119">Первичный ключ</span><span class="sxs-lookup"><span data-stu-id="0cf83-119">The primary key</span></span>

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

### <span data-ttu-id="0cf83-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cf83-120">-ResourceGroupName</span></span>
<span data-ttu-id="0cf83-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0cf83-121">Resource Group Name</span></span>

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

### <span data-ttu-id="0cf83-122">-Права</span><span class="sxs-lookup"><span data-stu-id="0cf83-122">-Rights</span></span>
<span data-ttu-id="0cf83-123">Разрешения для этого IOTHub</span><span class="sxs-lookup"><span data-stu-id="0cf83-123">The permissions for this IOTHub</span></span>

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

### <span data-ttu-id="0cf83-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="0cf83-124">-SecondaryKey</span></span>
<span data-ttu-id="0cf83-125">Вторичный ключ</span><span class="sxs-lookup"><span data-stu-id="0cf83-125">The Secondary Key</span></span>

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

### <span data-ttu-id="0cf83-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0cf83-126">-Confirm</span></span>
<span data-ttu-id="0cf83-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0cf83-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cf83-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cf83-128">-WhatIf</span></span>
<span data-ttu-id="0cf83-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0cf83-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cf83-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0cf83-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cf83-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cf83-131">CommonParameters</span></span>
<span data-ttu-id="0cf83-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0cf83-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cf83-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cf83-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cf83-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0cf83-134">INPUTS</span></span>

### <span data-ttu-id="0cf83-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0cf83-135">System.String</span></span>

## <span data-ttu-id="0cf83-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0cf83-136">OUTPUTS</span></span>

### <span data-ttu-id="0cf83-137">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0cf83-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="0cf83-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="0cf83-138">NOTES</span></span>

## <span data-ttu-id="0cf83-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0cf83-139">RELATED LINKS</span></span>
