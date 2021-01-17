---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
ms.openlocfilehash: b4cbecd2e29a0b70c7e62194df2364b22b33b462
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420900"
---
# <span data-ttu-id="54afa-101">Remove-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="54afa-101">Remove-AzSecurityContact</span></span>

## <span data-ttu-id="54afa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54afa-102">SYNOPSIS</span></span>
<span data-ttu-id="54afa-103">Удаляет контакт безопасности.</span><span class="sxs-lookup"><span data-stu-id="54afa-103">Deletes a security contact.</span></span>

## <span data-ttu-id="54afa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="54afa-104">SYNTAX</span></span>

### <span data-ttu-id="54afa-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="54afa-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54afa-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="54afa-106">ResourceId</span></span>
```
Remove-AzSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54afa-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="54afa-107">InputObject</span></span>
```
Remove-AzSecurityContact -InputObject <PSSecurityContact> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54afa-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54afa-108">DESCRIPTION</span></span>
<span data-ttu-id="54afa-109">Удаляет контакт безопасности.</span><span class="sxs-lookup"><span data-stu-id="54afa-109">Deletes a security contact.</span></span>

## <span data-ttu-id="54afa-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="54afa-110">EXAMPLES</span></span>

### <span data-ttu-id="54afa-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="54afa-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityContact -Name "default1"
```

<span data-ttu-id="54afa-112">Удаление контакта безопасности по умолчанию 1</span><span class="sxs-lookup"><span data-stu-id="54afa-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="54afa-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54afa-113">PARAMETERS</span></span>

### <span data-ttu-id="54afa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54afa-114">-DefaultProfile</span></span>
<span data-ttu-id="54afa-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54afa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54afa-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54afa-116">-InputObject</span></span>
<span data-ttu-id="54afa-117">Объект ввода.</span><span class="sxs-lookup"><span data-stu-id="54afa-117">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54afa-118">-Name</span><span class="sxs-lookup"><span data-stu-id="54afa-118">-Name</span></span>
<span data-ttu-id="54afa-119">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="54afa-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54afa-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54afa-120">-PassThru</span></span>
<span data-ttu-id="54afa-121">Возвращает, была ли операция успешной.</span><span class="sxs-lookup"><span data-stu-id="54afa-121">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="54afa-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54afa-122">-ResourceId</span></span>
<span data-ttu-id="54afa-123">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="54afa-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54afa-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54afa-124">-Confirm</span></span>
<span data-ttu-id="54afa-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="54afa-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54afa-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54afa-126">-WhatIf</span></span>
<span data-ttu-id="54afa-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54afa-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54afa-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="54afa-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54afa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54afa-129">CommonParameters</span></span>
<span data-ttu-id="54afa-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54afa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54afa-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54afa-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54afa-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54afa-132">INPUTS</span></span>

### <span data-ttu-id="54afa-133">System.String</span><span class="sxs-lookup"><span data-stu-id="54afa-133">System.String</span></span>

### <span data-ttu-id="54afa-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="54afa-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="54afa-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="54afa-135">OUTPUTS</span></span>

### <span data-ttu-id="54afa-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="54afa-136">System.Boolean</span></span>

## <span data-ttu-id="54afa-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="54afa-137">NOTES</span></span>

## <span data-ttu-id="54afa-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54afa-138">RELATED LINKS</span></span>
