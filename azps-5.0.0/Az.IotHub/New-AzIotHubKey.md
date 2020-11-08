---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
ms.openlocfilehash: cc843ca942ae79fe76e1dd50e76c876e4d05b5ac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247738"
---
# <span data-ttu-id="e2038-101">New-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="e2038-101">New-AzIotHubKey</span></span>

## <span data-ttu-id="e2038-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2038-102">SYNOPSIS</span></span>
<span data-ttu-id="e2038-103">Создание ключа центра Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="e2038-103">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="e2038-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2038-104">SYNTAX</span></span>

### <span data-ttu-id="e2038-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2038-105">ResourceSet (Default)</span></span>
```
New-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2038-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e2038-106">ResourceIdSet</span></span>
```
New-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2038-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2038-107">DESCRIPTION</span></span>
<span data-ttu-id="e2038-108">Создание ключа центра Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="e2038-108">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="e2038-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2038-109">EXAMPLES</span></span>

### <span data-ttu-id="e2038-110">Пример 1 повторное создание первичного ключа</span><span class="sxs-lookup"><span data-stu-id="e2038-110">Example 1 Regenerate primary key</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "primary"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=    6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=        ServiceConnect
```

<span data-ttu-id="e2038-111">Повторно создан первичный ключ для политики авторизации "testKey" центра Azure IOT.</span><span class="sxs-lookup"><span data-stu-id="e2038-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span></span>

### <span data-ttu-id="e2038-112">Пример 2 клавиши для замены</span><span class="sxs-lookup"><span data-stu-id="e2038-112">Example 2 Swapping keys</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "swap"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=    SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=        ServiceConnect
```

<span data-ttu-id="e2038-113">Переключение клавиш для политики авторизации "testKey" центра Azure IOT.</span><span class="sxs-lookup"><span data-stu-id="e2038-113">Swapping keys for the authorization policy "testKey" of an azure iot hub.</span></span>

## <span data-ttu-id="e2038-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2038-114">PARAMETERS</span></span>

### <span data-ttu-id="e2038-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2038-115">-DefaultProfile</span></span>
<span data-ttu-id="e2038-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e2038-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2038-117">-HubId</span><span class="sxs-lookup"><span data-stu-id="e2038-117">-HubId</span></span>
<span data-ttu-id="e2038-118">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="e2038-118">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e2038-119">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e2038-119">-KeyName</span></span>
<span data-ttu-id="e2038-120">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="e2038-120">Name of the Key</span></span>

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

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2038-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e2038-121">-Name</span></span>
<span data-ttu-id="e2038-122">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="e2038-122">Name of the IotHub</span></span>

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

### <span data-ttu-id="e2038-123">-RenewKey</span><span class="sxs-lookup"><span data-stu-id="e2038-123">-RenewKey</span></span>
<span data-ttu-id="e2038-124">Повторное создание ключа.</span><span class="sxs-lookup"><span data-stu-id="e2038-124">Regenerate Key.</span></span>

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

### <span data-ttu-id="e2038-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2038-125">-ResourceGroupName</span></span>
<span data-ttu-id="e2038-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e2038-126">Resource Group Name</span></span>

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

### <span data-ttu-id="e2038-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2038-127">-Confirm</span></span>
<span data-ttu-id="e2038-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e2038-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2038-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2038-129">-WhatIf</span></span>
<span data-ttu-id="e2038-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e2038-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2038-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e2038-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2038-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2038-132">CommonParameters</span></span>
<span data-ttu-id="e2038-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2038-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2038-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2038-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2038-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2038-135">INPUTS</span></span>

### <span data-ttu-id="e2038-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e2038-136">System.String</span></span>

## <span data-ttu-id="e2038-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2038-137">OUTPUTS</span></span>

### <span data-ttu-id="e2038-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e2038-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="e2038-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2038-139">NOTES</span></span>

## <span data-ttu-id="e2038-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2038-140">RELATED LINKS</span></span>
