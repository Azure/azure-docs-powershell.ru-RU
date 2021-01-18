---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
ms.openlocfilehash: 9074de6f4e6ee02a1476c1112d870b45d5bf6ccf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519034"
---
# <span data-ttu-id="f430d-101">Set-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="f430d-101">Set-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="f430d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f430d-102">SYNOPSIS</span></span>
<span data-ttu-id="f430d-103">Задает новый пароль для пользователя на устройстве.</span><span class="sxs-lookup"><span data-stu-id="f430d-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="f430d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f430d-104">SYNTAX</span></span>

### <span data-ttu-id="f430d-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f430d-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f430d-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f430d-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f430d-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f430d-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -InputObject <PSDataBoxEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f430d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f430d-108">DESCRIPTION</span></span>
<span data-ttu-id="f430d-109">С **помощью cmdlet set-AzDataBoxEdgeUser** можно установить новый пароль пользователя на устройстве Edge Data Box.</span><span class="sxs-lookup"><span data-stu-id="f430d-109">The **Set-AzDataBoxEdgeUser** cmdlet sets a new password for a user on the Data Box Edge device.</span></span>

## <span data-ttu-id="f430d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f430d-110">EXAMPLES</span></span>

### <span data-ttu-id="f430d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f430d-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="f430d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f430d-112">PARAMETERS</span></span>

### <span data-ttu-id="f430d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f430d-113">-AsJob</span></span>
<span data-ttu-id="f430d-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f430d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f430d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f430d-115">-DefaultProfile</span></span>
<span data-ttu-id="f430d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f430d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f430d-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f430d-117">-DeviceName</span></span>
<span data-ttu-id="f430d-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="f430d-118">Device Name</span></span>

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

### <span data-ttu-id="f430d-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f430d-119">-EncryptionKey</span></span>
<span data-ttu-id="f430d-120">Ключ шифрования устройства Edge</span><span class="sxs-lookup"><span data-stu-id="f430d-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="f430d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f430d-121">-InputObject</span></span>
<span data-ttu-id="f430d-122">Объект Input</span><span class="sxs-lookup"><span data-stu-id="f430d-122">Input Object</span></span>

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

### <span data-ttu-id="f430d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f430d-123">-Name</span></span>
<span data-ttu-id="f430d-124">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="f430d-124">Username</span></span>

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

### <span data-ttu-id="f430d-125">-Password</span><span class="sxs-lookup"><span data-stu-id="f430d-125">-Password</span></span>
<span data-ttu-id="f430d-126">Пароль в качестве защищенной строки</span><span class="sxs-lookup"><span data-stu-id="f430d-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="f430d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f430d-127">-ResourceGroupName</span></span>
<span data-ttu-id="f430d-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f430d-128">Resource Group Name</span></span>

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

### <span data-ttu-id="f430d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f430d-129">-ResourceId</span></span>
<span data-ttu-id="f430d-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f430d-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="f430d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f430d-131">-Confirm</span></span>
<span data-ttu-id="f430d-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f430d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f430d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f430d-133">-WhatIf</span></span>
<span data-ttu-id="f430d-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f430d-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f430d-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f430d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f430d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f430d-136">CommonParameters</span></span>
<span data-ttu-id="f430d-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f430d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f430d-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f430d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f430d-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f430d-139">INPUTS</span></span>

### <span data-ttu-id="f430d-140">Нет</span><span class="sxs-lookup"><span data-stu-id="f430d-140">None</span></span>

## <span data-ttu-id="f430d-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f430d-141">OUTPUTS</span></span>

### <span data-ttu-id="f430d-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="f430d-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="f430d-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f430d-143">NOTES</span></span>

## <span data-ttu-id="f430d-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f430d-144">RELATED LINKS</span></span>
