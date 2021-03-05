---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/set-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
ms.openlocfilehash: 0c3494e96290702c424a8e8bac7680daa376c488
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994871"
---
# <span data-ttu-id="8b240-101">Set-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="8b240-101">Set-AzStackEdgeUser</span></span>

## <span data-ttu-id="8b240-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b240-102">SYNOPSIS</span></span>
<span data-ttu-id="8b240-103">Задает новый пароль для пользователя на устройстве.</span><span class="sxs-lookup"><span data-stu-id="8b240-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="8b240-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8b240-104">SYNTAX</span></span>

### <span data-ttu-id="8b240-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8b240-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b240-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b240-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b240-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b240-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeUser -InputObject <PSStackEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b240-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b240-108">DESCRIPTION</span></span>
<span data-ttu-id="8b240-109">С **помощью cmdlet Set-AzStackEdgeUser** можно установить новый пароль для пользователя на устройстве Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="8b240-109">The **Set-AzStackEdgeUser** cmdlet sets a new password for a user on the Stack Edge device.</span></span>

## <span data-ttu-id="8b240-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8b240-110">EXAMPLES</span></span>

### <span data-ttu-id="8b240-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b240-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="8b240-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b240-112">PARAMETERS</span></span>

### <span data-ttu-id="8b240-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b240-113">-AsJob</span></span>
<span data-ttu-id="8b240-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8b240-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b240-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b240-115">-DefaultProfile</span></span>
<span data-ttu-id="8b240-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b240-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b240-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8b240-117">-DeviceName</span></span>
<span data-ttu-id="8b240-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="8b240-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b240-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="8b240-119">-EncryptionKey</span></span>
<span data-ttu-id="8b240-120">Ключ шифрования устройства Edge</span><span class="sxs-lookup"><span data-stu-id="8b240-120">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b240-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b240-121">-InputObject</span></span>
<span data-ttu-id="8b240-122">Объект Input</span><span class="sxs-lookup"><span data-stu-id="8b240-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases: User

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b240-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8b240-123">-Name</span></span>
<span data-ttu-id="8b240-124">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="8b240-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b240-125">-Password</span><span class="sxs-lookup"><span data-stu-id="8b240-125">-Password</span></span>
<span data-ttu-id="8b240-126">Пароль в качестве защищенной строки</span><span class="sxs-lookup"><span data-stu-id="8b240-126">Password, provide as a secure string</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b240-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b240-127">-ResourceGroupName</span></span>
<span data-ttu-id="8b240-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8b240-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b240-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b240-129">-ResourceId</span></span>
<span data-ttu-id="8b240-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b240-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b240-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b240-131">-Confirm</span></span>
<span data-ttu-id="8b240-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8b240-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b240-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b240-133">-WhatIf</span></span>
<span data-ttu-id="8b240-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b240-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b240-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8b240-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b240-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b240-136">CommonParameters</span></span>
<span data-ttu-id="8b240-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b240-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b240-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b240-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b240-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b240-139">INPUTS</span></span>

### <span data-ttu-id="8b240-140">Нет</span><span class="sxs-lookup"><span data-stu-id="8b240-140">None</span></span>

## <span data-ttu-id="8b240-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8b240-141">OUTPUTS</span></span>

### <span data-ttu-id="8b240-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="8b240-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="8b240-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8b240-143">NOTES</span></span>

## <span data-ttu-id="8b240-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b240-144">RELATED LINKS</span></span>
