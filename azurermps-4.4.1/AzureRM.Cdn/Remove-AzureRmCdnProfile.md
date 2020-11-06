---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
ms.openlocfilehash: f564a026359042a20e5d82e34425e98f1021422b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565637"
---
# <span data-ttu-id="632e5-101">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="632e5-101">Remove-AzureRmCdnProfile</span></span>

## <span data-ttu-id="632e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="632e5-102">SYNOPSIS</span></span>
<span data-ttu-id="632e5-103">Удаление профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="632e5-103">Removes a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="632e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="632e5-104">SYNTAX</span></span>

### <span data-ttu-id="632e5-105">Наборы параметров для параметров полей</span><span class="sxs-lookup"><span data-stu-id="632e5-105">Parameter Set for fields parameters</span></span>
```
Remove-AzureRmCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="632e5-106">Параметр, заданный для параметров объекта</span><span class="sxs-lookup"><span data-stu-id="632e5-106">Parameter Set for object parameters</span></span>
```
Remove-AzureRmCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="632e5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="632e5-107">DESCRIPTION</span></span>
<span data-ttu-id="632e5-108">Командлет **Remove-AzureRmCdnProfile** удаляет профиль сети доставки содержимого (CDN) для Azure.</span><span class="sxs-lookup"><span data-stu-id="632e5-108">The **Remove-AzureRmCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="632e5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="632e5-109">EXAMPLES</span></span>

## <span data-ttu-id="632e5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="632e5-110">PARAMETERS</span></span>

### <span data-ttu-id="632e5-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="632e5-111">-CdnProfile</span></span>
<span data-ttu-id="632e5-112">Указывает профиль, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="632e5-112">Specifies the profile that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="632e5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="632e5-113">-Force</span></span>
<span data-ttu-id="632e5-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="632e5-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="632e5-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="632e5-115">-PassThru</span></span>
<span data-ttu-id="632e5-116">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="632e5-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="632e5-117">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="632e5-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="632e5-118">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="632e5-118">-ProfileName</span></span>
<span data-ttu-id="632e5-119">Указывает имя профиля, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="632e5-119">Specifies the name of the profile that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632e5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="632e5-120">-ResourceGroupName</span></span>
<span data-ttu-id="632e5-121">Указывает имя группы ресурсов, к которой относится профиль.</span><span class="sxs-lookup"><span data-stu-id="632e5-121">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632e5-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="632e5-122">-Confirm</span></span>
<span data-ttu-id="632e5-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="632e5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="632e5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="632e5-124">-WhatIf</span></span>
<span data-ttu-id="632e5-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="632e5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="632e5-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="632e5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="632e5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="632e5-127">-DefaultProfile</span></span>
<span data-ttu-id="632e5-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="632e5-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="632e5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="632e5-129">CommonParameters</span></span>
<span data-ttu-id="632e5-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="632e5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="632e5-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="632e5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="632e5-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="632e5-132">INPUTS</span></span>

### <span data-ttu-id="632e5-133">PSProfile</span><span class="sxs-lookup"><span data-stu-id="632e5-133">PSProfile</span></span>
<span data-ttu-id="632e5-134">Параметр "CdnProfile" принимает значение типа "PSProfile" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="632e5-134">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="632e5-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="632e5-135">OUTPUTS</span></span>

### <span data-ttu-id="632e5-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="632e5-136">System.Boolean</span></span>

## <span data-ttu-id="632e5-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="632e5-137">NOTES</span></span>

## <span data-ttu-id="632e5-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="632e5-138">RELATED LINKS</span></span>

[<span data-ttu-id="632e5-139">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="632e5-139">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="632e5-140">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="632e5-140">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="632e5-141">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="632e5-141">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


