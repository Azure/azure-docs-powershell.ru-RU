---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
ms.openlocfilehash: 9074de6f4e6ee02a1476c1112d870b45d5bf6ccf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401775"
---
# <span data-ttu-id="14787-101">Set-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="14787-101">Set-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="14787-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14787-102">SYNOPSIS</span></span>
<span data-ttu-id="14787-103">Задает новый пароль для пользователя на устройстве.</span><span class="sxs-lookup"><span data-stu-id="14787-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="14787-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="14787-104">SYNTAX</span></span>

### <span data-ttu-id="14787-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="14787-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14787-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14787-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14787-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14787-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -InputObject <PSDataBoxEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14787-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14787-108">DESCRIPTION</span></span>
<span data-ttu-id="14787-109">С **помощью cmdlet set-AzDataBoxEdgeUser** можно установить новый пароль пользователя на устройстве Edge Data Box.</span><span class="sxs-lookup"><span data-stu-id="14787-109">The **Set-AzDataBoxEdgeUser** cmdlet sets a new password for a user on the Data Box Edge device.</span></span>

## <span data-ttu-id="14787-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="14787-110">EXAMPLES</span></span>

### <span data-ttu-id="14787-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="14787-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="14787-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14787-112">PARAMETERS</span></span>

### <span data-ttu-id="14787-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14787-113">-AsJob</span></span>
<span data-ttu-id="14787-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="14787-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14787-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14787-115">-DefaultProfile</span></span>
<span data-ttu-id="14787-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14787-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14787-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="14787-117">-DeviceName</span></span>
<span data-ttu-id="14787-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="14787-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14787-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="14787-119">-EncryptionKey</span></span>
<span data-ttu-id="14787-120">Ключ шифрования устройства Edge</span><span class="sxs-lookup"><span data-stu-id="14787-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="14787-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14787-121">-InputObject</span></span>
<span data-ttu-id="14787-122">Объект Input</span><span class="sxs-lookup"><span data-stu-id="14787-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14787-123">-Name</span><span class="sxs-lookup"><span data-stu-id="14787-123">-Name</span></span>
<span data-ttu-id="14787-124">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="14787-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14787-125">-Password</span><span class="sxs-lookup"><span data-stu-id="14787-125">-Password</span></span>
<span data-ttu-id="14787-126">Пароль в качестве защищенной строки</span><span class="sxs-lookup"><span data-stu-id="14787-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="14787-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14787-127">-ResourceGroupName</span></span>
<span data-ttu-id="14787-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="14787-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14787-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14787-129">-ResourceId</span></span>
<span data-ttu-id="14787-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="14787-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14787-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14787-131">-Confirm</span></span>
<span data-ttu-id="14787-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="14787-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14787-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14787-133">-WhatIf</span></span>
<span data-ttu-id="14787-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14787-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14787-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="14787-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14787-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14787-136">CommonParameters</span></span>
<span data-ttu-id="14787-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14787-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14787-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14787-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14787-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14787-139">INPUTS</span></span>

### <span data-ttu-id="14787-140">Нет</span><span class="sxs-lookup"><span data-stu-id="14787-140">None</span></span>

## <span data-ttu-id="14787-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="14787-141">OUTPUTS</span></span>

### <span data-ttu-id="14787-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="14787-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="14787-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="14787-143">NOTES</span></span>

## <span data-ttu-id="14787-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14787-144">RELATED LINKS</span></span>
