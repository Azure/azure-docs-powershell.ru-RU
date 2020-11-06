---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
ms.openlocfilehash: 0c39e6ee26faffc9c12e2fc3b5f00ccaadfa9389
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565889"
---
# <span data-ttu-id="3770b-101">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="3770b-101">Remove-AzureRmCdnProfile</span></span>

## <span data-ttu-id="3770b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3770b-102">SYNOPSIS</span></span>
<span data-ttu-id="3770b-103">Удаление профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="3770b-103">Removes a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3770b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3770b-104">SYNTAX</span></span>

### <span data-ttu-id="3770b-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="3770b-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3770b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3770b-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3770b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3770b-107">DESCRIPTION</span></span>
<span data-ttu-id="3770b-108">Командлет **Remove-AzureRmCdnProfile** удаляет профиль сети доставки содержимого (CDN) для Azure.</span><span class="sxs-lookup"><span data-stu-id="3770b-108">The **Remove-AzureRmCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="3770b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3770b-109">EXAMPLES</span></span>

## <span data-ttu-id="3770b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3770b-110">PARAMETERS</span></span>

### <span data-ttu-id="3770b-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="3770b-111">-CdnProfile</span></span>
<span data-ttu-id="3770b-112">Указывает профиль, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3770b-112">Specifies the profile that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3770b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3770b-113">-DefaultProfile</span></span>
<span data-ttu-id="3770b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3770b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3770b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3770b-115">-Force</span></span>
<span data-ttu-id="3770b-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="3770b-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3770b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3770b-117">-PassThru</span></span>
<span data-ttu-id="3770b-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="3770b-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3770b-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3770b-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3770b-120">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="3770b-120">-ProfileName</span></span>
<span data-ttu-id="3770b-121">Указывает имя профиля, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="3770b-121">Specifies the name of the profile that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3770b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3770b-122">-ResourceGroupName</span></span>
<span data-ttu-id="3770b-123">Указывает имя группы ресурсов, к которой относится профиль.</span><span class="sxs-lookup"><span data-stu-id="3770b-123">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3770b-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3770b-124">-Confirm</span></span>
<span data-ttu-id="3770b-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3770b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3770b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3770b-126">-WhatIf</span></span>
<span data-ttu-id="3770b-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3770b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3770b-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3770b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3770b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3770b-129">CommonParameters</span></span>
<span data-ttu-id="3770b-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3770b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3770b-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3770b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3770b-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3770b-132">INPUTS</span></span>

### <span data-ttu-id="3770b-133">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="3770b-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="3770b-134">Параметры: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3770b-134">Parameters: CdnProfile (ByValue)</span></span>

### <span data-ttu-id="3770b-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3770b-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3770b-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3770b-136">OUTPUTS</span></span>

### <span data-ttu-id="3770b-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3770b-137">System.Boolean</span></span>

## <span data-ttu-id="3770b-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="3770b-138">NOTES</span></span>

## <span data-ttu-id="3770b-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3770b-139">RELATED LINKS</span></span>

[<span data-ttu-id="3770b-140">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="3770b-140">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="3770b-141">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="3770b-141">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="3770b-142">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="3770b-142">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


