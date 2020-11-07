---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
ms.openlocfilehash: 8e75965b4f69315b6ab94fa7c77e3859e11a4f45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720719"
---
# <span data-ttu-id="6b969-101">New-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="6b969-101">New-AzIotHubKey</span></span>

## <span data-ttu-id="6b969-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b969-102">SYNOPSIS</span></span>
<span data-ttu-id="6b969-103">Создание ключа центра Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="6b969-103">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="6b969-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b969-104">SYNTAX</span></span>

### <span data-ttu-id="6b969-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6b969-105">ResourceSet (Default)</span></span>
```
New-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b969-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6b969-106">ResourceIdSet</span></span>
```
New-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b969-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b969-107">DESCRIPTION</span></span>
<span data-ttu-id="6b969-108">Создание ключа центра Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="6b969-108">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="6b969-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b969-109">EXAMPLES</span></span>

### <span data-ttu-id="6b969-110">Пример 1 повторное создание первичного ключа</span><span class="sxs-lookup"><span data-stu-id="6b969-110">Example 1 Regenerate primary key</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "primary"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=    6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=        ServiceConnect
```

<span data-ttu-id="6b969-111">Повторно создан первичный ключ для политики авторизации "testKey" центра Azure IOT.</span><span class="sxs-lookup"><span data-stu-id="6b969-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span></span>

### <span data-ttu-id="6b969-112">Пример 2 клавиши для замены</span><span class="sxs-lookup"><span data-stu-id="6b969-112">Example 2 Swapping keys</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "swap"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=    SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=        ServiceConnect
```

<span data-ttu-id="6b969-113">Переключение клавиш для политики авторизации "testKey" центра Azure IOT.</span><span class="sxs-lookup"><span data-stu-id="6b969-113">Swapping keys for the authorization policy "testKey" of an azure iot hub.</span></span>

## <span data-ttu-id="6b969-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b969-114">PARAMETERS</span></span>

### <span data-ttu-id="6b969-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b969-115">-DefaultProfile</span></span>
<span data-ttu-id="6b969-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6b969-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b969-117">-HubId</span><span class="sxs-lookup"><span data-stu-id="6b969-117">-HubId</span></span>
<span data-ttu-id="6b969-118">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="6b969-118">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6b969-119">-KeyName</span><span class="sxs-lookup"><span data-stu-id="6b969-119">-KeyName</span></span>
<span data-ttu-id="6b969-120">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="6b969-120">Name of the Key</span></span>

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

### <span data-ttu-id="6b969-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6b969-121">-Name</span></span>
<span data-ttu-id="6b969-122">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="6b969-122">Name of the IotHub</span></span>

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

### <span data-ttu-id="6b969-123">-RenewKey</span><span class="sxs-lookup"><span data-stu-id="6b969-123">-RenewKey</span></span>
<span data-ttu-id="6b969-124">Повторное создание ключа.</span><span class="sxs-lookup"><span data-stu-id="6b969-124">Regenerate Key.</span></span>

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

### <span data-ttu-id="6b969-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b969-125">-ResourceGroupName</span></span>
<span data-ttu-id="6b969-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6b969-126">Resource Group Name</span></span>

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

### <span data-ttu-id="6b969-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b969-127">-Confirm</span></span>
<span data-ttu-id="6b969-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6b969-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b969-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b969-129">-WhatIf</span></span>
<span data-ttu-id="6b969-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6b969-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b969-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6b969-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b969-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b969-132">CommonParameters</span></span>
<span data-ttu-id="6b969-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b969-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b969-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b969-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b969-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b969-135">INPUTS</span></span>

### <span data-ttu-id="6b969-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6b969-136">System.String</span></span>

## <span data-ttu-id="6b969-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b969-137">OUTPUTS</span></span>

### <span data-ttu-id="6b969-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6b969-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="6b969-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b969-139">NOTES</span></span>

## <span data-ttu-id="6b969-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b969-140">RELATED LINKS</span></span>
