---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
ms.openlocfilehash: 81cb94cdcb8efa948160d21da3aca709bb86b6fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562632"
---
# <span data-ttu-id="8ab29-101">Set-AzureRmSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="8ab29-101">Set-AzureRmSecurityAlert</span></span>

## <span data-ttu-id="8ab29-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ab29-102">SYNOPSIS</span></span>
<span data-ttu-id="8ab29-103">Обновляет состояние оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="8ab29-103">Updates a security alert state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ab29-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ab29-104">SYNTAX</span></span>

### <span data-ttu-id="8ab29-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ab29-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ab29-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="8ab29-106">ResourceGroupLevelResource</span></span>
```
Set-AzureRmSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ab29-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ab29-107">ResourceId</span></span>
```
Set-AzureRmSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ab29-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="8ab29-108">InputObject</span></span>
```
Set-AzureRmSecurityAlert [-ActionType <String>] -InputObject <PSSetAlertInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ab29-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ab29-109">DESCRIPTION</span></span>
<span data-ttu-id="8ab29-110">Задает состояние оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="8ab29-110">Sets a security alert state.</span></span>

## <span data-ttu-id="8ab29-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ab29-111">EXAMPLES</span></span>

### <span data-ttu-id="8ab29-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8ab29-112">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="8ab29-113">Закрывает возникшее оповещение системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="8ab29-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="8ab29-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ab29-114">PARAMETERS</span></span>

### <span data-ttu-id="8ab29-115">-Себя</span><span class="sxs-lookup"><span data-stu-id="8ab29-115">-ActionType</span></span>
<span data-ttu-id="8ab29-116">Тип действия.</span><span class="sxs-lookup"><span data-stu-id="8ab29-116">Action Type.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab29-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ab29-117">-DefaultProfile</span></span>
<span data-ttu-id="8ab29-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ab29-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ab29-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ab29-119">-InputObject</span></span>
<span data-ttu-id="8ab29-120">Объект input.</span><span class="sxs-lookup"><span data-stu-id="8ab29-120">Input Object.</span></span>

```yaml
Type: PSSetAlertInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab29-121">-Location</span><span class="sxs-lookup"><span data-stu-id="8ab29-121">-Location</span></span>
<span data-ttu-id="8ab29-122">Поиска.</span><span class="sxs-lookup"><span data-stu-id="8ab29-122">Location.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab29-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8ab29-123">-Name</span></span>
<span data-ttu-id="8ab29-124">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="8ab29-124">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab29-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ab29-125">-PassThru</span></span>
<span data-ttu-id="8ab29-126">Возвращает значение, указывающее, была ли операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8ab29-126">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab29-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ab29-127">-ResourceGroupName</span></span>
<span data-ttu-id="8ab29-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ab29-128">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab29-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ab29-129">-ResourceId</span></span>
<span data-ttu-id="8ab29-130">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="8ab29-130">Resource ID.</span></span>

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

### <span data-ttu-id="8ab29-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ab29-131">-Confirm</span></span>
<span data-ttu-id="8ab29-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8ab29-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab29-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ab29-133">-WhatIf</span></span>
<span data-ttu-id="8ab29-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8ab29-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ab29-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8ab29-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab29-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ab29-136">CommonParameters</span></span>
<span data-ttu-id="8ab29-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ab29-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ab29-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ab29-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ab29-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ab29-139">INPUTS</span></span>

### <span data-ttu-id="8ab29-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8ab29-140">System.String</span></span>
<span data-ttu-id="8ab29-141">Microsoft. Azure. Commands. Security. командлеты. Alerts. PSSetAlertInputObject</span><span class="sxs-lookup"><span data-stu-id="8ab29-141">Microsoft.Azure.Commands.Security.Cmdlets.Alerts.PSSetAlertInputObject</span></span>

## <span data-ttu-id="8ab29-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ab29-142">OUTPUTS</span></span>

### <span data-ttu-id="8ab29-143">Microsoft. Azure. Commands. Security. Models. Alerts. PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="8ab29-143">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="8ab29-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ab29-144">NOTES</span></span>

## <span data-ttu-id="8ab29-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ab29-145">RELATED LINKS</span></span>
