---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 19de4ad776814efa55cdff19b2a77673d8581992
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562640"
---
# <span data-ttu-id="5cdc4-101">Remove-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5cdc4-101">Remove-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="5cdc4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5cdc4-102">SYNOPSIS</span></span>
<span data-ttu-id="5cdc4-103">Удаление политики доступа по JIT-сети.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-103">Deletes a JIT network access policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cdc4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5cdc4-104">SYNTAX</span></span>

### <span data-ttu-id="5cdc4-105">ResourceGroupLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5cdc4-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cdc4-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5cdc4-106">ResourceId</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cdc4-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="5cdc4-107">InputObject</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -InputObject <PSRemoveJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cdc4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5cdc4-108">DESCRIPTION</span></span>
<span data-ttu-id="5cdc4-109">Удаление политики сетевого доступа по времени.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="5cdc4-110">После этого пользователь не сможет запросить временное сетевое подключение на виртуальных машинах, настроенных в удаленной политике.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="5cdc4-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5cdc4-111">EXAMPLES</span></span>

### <span data-ttu-id="5cdc4-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5cdc4-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="5cdc4-113">Удаление политики сетевого доступа по времени.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="5cdc4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5cdc4-114">PARAMETERS</span></span>

### <span data-ttu-id="5cdc4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cdc4-115">-DefaultProfile</span></span>
<span data-ttu-id="5cdc4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cdc4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cdc4-117">-InputObject</span></span>
<span data-ttu-id="5cdc4-118">Объект input.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-118">Input Object.</span></span>

```yaml
Type: PSRemoveJitNetworkAccessPolicy
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cdc4-119">-Location</span><span class="sxs-lookup"><span data-stu-id="5cdc4-119">-Location</span></span>
<span data-ttu-id="5cdc4-120">Поиска.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-120">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cdc4-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5cdc4-121">-Name</span></span>
<span data-ttu-id="5cdc4-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cdc4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5cdc4-123">-PassThru</span></span>
<span data-ttu-id="5cdc4-124">Возвращает значение, указывающее, была ли операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="5cdc4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cdc4-125">-ResourceGroupName</span></span>
<span data-ttu-id="5cdc4-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-126">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cdc4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5cdc4-127">-ResourceId</span></span>
<span data-ttu-id="5cdc4-128">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-128">Resource ID.</span></span>

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

### <span data-ttu-id="5cdc4-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5cdc4-129">-Confirm</span></span>
<span data-ttu-id="5cdc4-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cdc4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cdc4-131">-WhatIf</span></span>
<span data-ttu-id="5cdc4-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5cdc4-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cdc4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cdc4-134">CommonParameters</span></span>
<span data-ttu-id="5cdc4-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5cdc4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cdc4-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cdc4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cdc4-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5cdc4-137">INPUTS</span></span>

### <span data-ttu-id="5cdc4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5cdc4-138">System.String</span></span>
<span data-ttu-id="5cdc4-139">Microsoft. Azure. Commands. Security. командлеты. JitNetworkAccessPolicies. PSRemoveJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5cdc4-139">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSRemoveJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="5cdc4-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5cdc4-140">OUTPUTS</span></span>

### <span data-ttu-id="5cdc4-141">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5cdc4-141">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="5cdc4-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="5cdc4-142">NOTES</span></span>

## <span data-ttu-id="5cdc4-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5cdc4-143">RELATED LINKS</span></span>
