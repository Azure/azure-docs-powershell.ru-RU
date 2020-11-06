---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
ms.openlocfilehash: 8c2f6a45bb483109b61be47de3013f3ccb4d5c19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567239"
---
# <span data-ttu-id="d09e4-101">Remove-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="d09e4-101">Remove-AzureRmSecurityContact</span></span>

## <span data-ttu-id="d09e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d09e4-102">SYNOPSIS</span></span>
<span data-ttu-id="d09e4-103">Удаление контакта безопасности.</span><span class="sxs-lookup"><span data-stu-id="d09e4-103">Deletes a security contact.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d09e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d09e4-104">SYNTAX</span></span>

### <span data-ttu-id="d09e4-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d09e4-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzureRmSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d09e4-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d09e4-106">ResourceId</span></span>
```
Remove-AzureRmSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d09e4-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d09e4-107">InputObject</span></span>
```
Remove-AzureRmSecurityContact -InputObject <PSRemoveSecurityContactInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d09e4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d09e4-108">DESCRIPTION</span></span>
<span data-ttu-id="d09e4-109">Удаление контакта безопасности.</span><span class="sxs-lookup"><span data-stu-id="d09e4-109">Deletes a security contact.</span></span>

## <span data-ttu-id="d09e4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d09e4-110">EXAMPLES</span></span>

### <span data-ttu-id="d09e4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d09e4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSecurityContact -Name "default1"
```

<span data-ttu-id="d09e4-112">Удаляет контакт безопасности "default1"</span><span class="sxs-lookup"><span data-stu-id="d09e4-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="d09e4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d09e4-113">PARAMETERS</span></span>

### <span data-ttu-id="d09e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d09e4-114">-DefaultProfile</span></span>
<span data-ttu-id="d09e4-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d09e4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d09e4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d09e4-116">-InputObject</span></span>
<span data-ttu-id="d09e4-117">Объект input.</span><span class="sxs-lookup"><span data-stu-id="d09e4-117">Input Object.</span></span>

```yaml
Type: PSRemoveSecurityContactInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d09e4-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d09e4-118">-Name</span></span>
<span data-ttu-id="d09e4-119">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="d09e4-119">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d09e4-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d09e4-120">-PassThru</span></span>
<span data-ttu-id="d09e4-121">Возвращает значение, указывающее, была ли операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d09e4-121">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="d09e4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d09e4-122">-ResourceId</span></span>
<span data-ttu-id="d09e4-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="d09e4-123">Resource ID.</span></span>

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

### <span data-ttu-id="d09e4-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d09e4-124">-Confirm</span></span>
<span data-ttu-id="d09e4-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d09e4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d09e4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d09e4-126">-WhatIf</span></span>
<span data-ttu-id="d09e4-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d09e4-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d09e4-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d09e4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d09e4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d09e4-129">CommonParameters</span></span>
<span data-ttu-id="d09e4-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d09e4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d09e4-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d09e4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d09e4-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d09e4-132">INPUTS</span></span>

### <span data-ttu-id="d09e4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d09e4-133">System.String</span></span>
<span data-ttu-id="d09e4-134">Microsoft. Azure. Commands. Security. командлеты. SecurityContacts. PSRemoveSecurityContactInputObject</span><span class="sxs-lookup"><span data-stu-id="d09e4-134">Microsoft.Azure.Commands.Security.Cmdlets.SecurityContacts.PSRemoveSecurityContactInputObject</span></span>

## <span data-ttu-id="d09e4-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d09e4-135">OUTPUTS</span></span>

### <span data-ttu-id="d09e4-136">Microsoft. Azure. Commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="d09e4-136">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="d09e4-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="d09e4-137">NOTES</span></span>

## <span data-ttu-id="d09e4-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d09e4-138">RELATED LINKS</span></span>
