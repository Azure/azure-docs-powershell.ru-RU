---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 1c6f6a38c1811bdda32b60d4af1707c78eb7afd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732581"
---
# <span data-ttu-id="c869a-101">Remove-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="c869a-101">Remove-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="c869a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c869a-102">SYNOPSIS</span></span>
<span data-ttu-id="c869a-103">Удаление параметра рабочей области безопасности для этой подписки.</span><span class="sxs-lookup"><span data-stu-id="c869a-103">Deletes the security workspace setting for this subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c869a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c869a-104">SYNTAX</span></span>

### <span data-ttu-id="c869a-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c869a-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c869a-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c869a-106">ResourceId</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c869a-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c869a-107">InputObject</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -InputObject <PSRemoveWorkspaceSettingInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c869a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c869a-108">DESCRIPTION</span></span>
<span data-ttu-id="c869a-109">Удаление параметра рабочей области безопасности для этой подписки.</span><span class="sxs-lookup"><span data-stu-id="c869a-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="c869a-110">С помощью этого действия новые установленные агенты безопасности будут сообщать о рабочей области этого susbscription по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c869a-110">This action will make the newly installed security agents to report to the default workspace of this susbscription.</span></span>

## <span data-ttu-id="c869a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c869a-111">EXAMPLES</span></span>

### <span data-ttu-id="c869a-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c869a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="c869a-113">Удаление параметра рабочей области безопасности для этой подписки.</span><span class="sxs-lookup"><span data-stu-id="c869a-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="c869a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c869a-114">PARAMETERS</span></span>

### <span data-ttu-id="c869a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c869a-115">-DefaultProfile</span></span>
<span data-ttu-id="c869a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c869a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c869a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c869a-117">-InputObject</span></span>
<span data-ttu-id="c869a-118">Объект input.</span><span class="sxs-lookup"><span data-stu-id="c869a-118">Input Object.</span></span>

```yaml
Type: PSRemoveWorkspaceSettingInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c869a-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c869a-119">-Name</span></span>
<span data-ttu-id="c869a-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="c869a-120">Resource name.</span></span>

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

### <span data-ttu-id="c869a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c869a-121">-PassThru</span></span>
<span data-ttu-id="c869a-122">Возвращает значение, указывающее, была ли операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c869a-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="c869a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c869a-123">-ResourceId</span></span>
<span data-ttu-id="c869a-124">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="c869a-124">Resource ID.</span></span>

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

### <span data-ttu-id="c869a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c869a-125">-Confirm</span></span>
<span data-ttu-id="c869a-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c869a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c869a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c869a-127">-WhatIf</span></span>
<span data-ttu-id="c869a-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c869a-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c869a-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c869a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c869a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c869a-130">CommonParameters</span></span>
<span data-ttu-id="c869a-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c869a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c869a-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c869a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c869a-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c869a-133">INPUTS</span></span>

### <span data-ttu-id="c869a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c869a-134">System.String</span></span>
<span data-ttu-id="c869a-135">Microsoft. Azure. Commands. Security. командлеты. WorkspaceSettings. PSRemoveWorkspaceSettingInputObject</span><span class="sxs-lookup"><span data-stu-id="c869a-135">Microsoft.Azure.Commands.Security.Cmdlets.WorkspaceSettings.PSRemoveWorkspaceSettingInputObject</span></span>

## <span data-ttu-id="c869a-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c869a-136">OUTPUTS</span></span>

### <span data-ttu-id="c869a-137">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="c869a-137">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="c869a-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="c869a-138">NOTES</span></span>

## <span data-ttu-id="c869a-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c869a-139">RELATED LINKS</span></span>
