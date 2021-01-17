---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
ms.openlocfilehash: 707889590efeb17ee676fe3d8b37325bc48fdc81
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404423"
---
# <span data-ttu-id="bdb31-101">Set-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="bdb31-101">Set-AzStackEdgeUser</span></span>

## <span data-ttu-id="bdb31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdb31-102">SYNOPSIS</span></span>
<span data-ttu-id="bdb31-103">Задает новый пароль для пользователя на устройстве.</span><span class="sxs-lookup"><span data-stu-id="bdb31-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="bdb31-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bdb31-104">SYNTAX</span></span>

### <span data-ttu-id="bdb31-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bdb31-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdb31-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdb31-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdb31-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdb31-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeUser -InputObject <PSStackEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdb31-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdb31-108">DESCRIPTION</span></span>
<span data-ttu-id="bdb31-109">С **помощью cmdlet Set-AzStackEdgeUser** можно установить новый пароль пользователя на устройстве Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="bdb31-109">The **Set-AzStackEdgeUser** cmdlet sets a new password for a user on the Stack Edge device.</span></span>

## <span data-ttu-id="bdb31-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bdb31-110">EXAMPLES</span></span>

### <span data-ttu-id="bdb31-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bdb31-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="bdb31-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdb31-112">PARAMETERS</span></span>

### <span data-ttu-id="bdb31-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdb31-113">-AsJob</span></span>
<span data-ttu-id="bdb31-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bdb31-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bdb31-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdb31-115">-DefaultProfile</span></span>
<span data-ttu-id="bdb31-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bdb31-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdb31-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="bdb31-117">-DeviceName</span></span>
<span data-ttu-id="bdb31-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="bdb31-118">Device Name</span></span>

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

### <span data-ttu-id="bdb31-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="bdb31-119">-EncryptionKey</span></span>
<span data-ttu-id="bdb31-120">Ключ шифрования устройства Edge</span><span class="sxs-lookup"><span data-stu-id="bdb31-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="bdb31-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdb31-121">-InputObject</span></span>
<span data-ttu-id="bdb31-122">Объект Input</span><span class="sxs-lookup"><span data-stu-id="bdb31-122">Input Object</span></span>

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

### <span data-ttu-id="bdb31-123">-Name</span><span class="sxs-lookup"><span data-stu-id="bdb31-123">-Name</span></span>
<span data-ttu-id="bdb31-124">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="bdb31-124">Username</span></span>

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

### <span data-ttu-id="bdb31-125">-Password</span><span class="sxs-lookup"><span data-stu-id="bdb31-125">-Password</span></span>
<span data-ttu-id="bdb31-126">Пароль в качестве защищенной строки</span><span class="sxs-lookup"><span data-stu-id="bdb31-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="bdb31-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdb31-127">-ResourceGroupName</span></span>
<span data-ttu-id="bdb31-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="bdb31-128">Resource Group Name</span></span>

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

### <span data-ttu-id="bdb31-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdb31-129">-ResourceId</span></span>
<span data-ttu-id="bdb31-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdb31-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="bdb31-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bdb31-131">-Confirm</span></span>
<span data-ttu-id="bdb31-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdb31-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdb31-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdb31-133">-WhatIf</span></span>
<span data-ttu-id="bdb31-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdb31-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bdb31-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bdb31-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdb31-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdb31-136">CommonParameters</span></span>
<span data-ttu-id="bdb31-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdb31-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdb31-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bdb31-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdb31-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bdb31-139">INPUTS</span></span>

### <span data-ttu-id="bdb31-140">Нет</span><span class="sxs-lookup"><span data-stu-id="bdb31-140">None</span></span>

## <span data-ttu-id="bdb31-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bdb31-141">OUTPUTS</span></span>

### <span data-ttu-id="bdb31-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="bdb31-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="bdb31-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bdb31-143">NOTES</span></span>

## <span data-ttu-id="bdb31-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bdb31-144">RELATED LINKS</span></span>
