---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
ms.openlocfilehash: 7dd27544e3304570cf3fbdae861b21eabd300c35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968979"
---
# <span data-ttu-id="c53dd-101">New-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="c53dd-101">New-AzIotHubKey</span></span>

## <span data-ttu-id="c53dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c53dd-102">SYNOPSIS</span></span>
<span data-ttu-id="c53dd-103">Создание ключа Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c53dd-103">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="c53dd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c53dd-104">SYNTAX</span></span>

### <span data-ttu-id="c53dd-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c53dd-105">ResourceSet (Default)</span></span>
```
New-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c53dd-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c53dd-106">ResourceIdSet</span></span>
```
New-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c53dd-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c53dd-107">DESCRIPTION</span></span>
<span data-ttu-id="c53dd-108">Создание ключа Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c53dd-108">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="c53dd-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c53dd-109">EXAMPLES</span></span>

### <span data-ttu-id="c53dd-110">Пример 1. Повторное сгенерировать первичный ключ</span><span class="sxs-lookup"><span data-stu-id="c53dd-110">Example 1 Regenerate primary key</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "primary"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=    6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=        ServiceConnect
```

<span data-ttu-id="c53dd-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span><span class="sxs-lookup"><span data-stu-id="c53dd-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span></span>

### <span data-ttu-id="c53dd-112">Пример 2: пере обмен ключами</span><span class="sxs-lookup"><span data-stu-id="c53dd-112">Example 2 Swapping keys</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "swap"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=    SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=        ServiceConnect
```

<span data-ttu-id="c53dd-113">Пере обмен ключами для политики авторизации testKey в azure iot Hub.</span><span class="sxs-lookup"><span data-stu-id="c53dd-113">Swapping keys for the authorization policy "testKey" of an azure iot hub.</span></span>

## <span data-ttu-id="c53dd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c53dd-114">PARAMETERS</span></span>

### <span data-ttu-id="c53dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c53dd-115">-DefaultProfile</span></span>
<span data-ttu-id="c53dd-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c53dd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c53dd-117">-HubId</span><span class="sxs-lookup"><span data-stu-id="c53dd-117">-HubId</span></span>
<span data-ttu-id="c53dd-118">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="c53dd-118">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c53dd-119">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c53dd-119">-KeyName</span></span>
<span data-ttu-id="c53dd-120">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="c53dd-120">Name of the Key</span></span>

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

### <span data-ttu-id="c53dd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c53dd-121">-Name</span></span>
<span data-ttu-id="c53dd-122">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="c53dd-122">Name of the IotHub</span></span>

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

### <span data-ttu-id="c53dd-123">-RenewKey</span><span class="sxs-lookup"><span data-stu-id="c53dd-123">-RenewKey</span></span>
<span data-ttu-id="c53dd-124">Повторно сгенерировать ключ.</span><span class="sxs-lookup"><span data-stu-id="c53dd-124">Regenerate Key.</span></span>

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

### <span data-ttu-id="c53dd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c53dd-125">-ResourceGroupName</span></span>
<span data-ttu-id="c53dd-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c53dd-126">Resource Group Name</span></span>

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

### <span data-ttu-id="c53dd-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c53dd-127">-Confirm</span></span>
<span data-ttu-id="c53dd-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c53dd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c53dd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c53dd-129">-WhatIf</span></span>
<span data-ttu-id="c53dd-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c53dd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c53dd-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c53dd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c53dd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c53dd-132">CommonParameters</span></span>
<span data-ttu-id="c53dd-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c53dd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c53dd-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c53dd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c53dd-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c53dd-135">INPUTS</span></span>

### <span data-ttu-id="c53dd-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c53dd-136">System.String</span></span>

## <span data-ttu-id="c53dd-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c53dd-137">OUTPUTS</span></span>

### <span data-ttu-id="c53dd-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c53dd-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="c53dd-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c53dd-139">NOTES</span></span>

## <span data-ttu-id="c53dd-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c53dd-140">RELATED LINKS</span></span>
