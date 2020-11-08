---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
ms.openlocfilehash: 707889590efeb17ee676fe3d8b37325bc48fdc81
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243196"
---
# <span data-ttu-id="97f86-101">Set-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="97f86-101">Set-AzStackEdgeUser</span></span>

## <span data-ttu-id="97f86-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="97f86-102">SYNOPSIS</span></span>
<span data-ttu-id="97f86-103">Установка нового пароля для пользователя на устройстве.</span><span class="sxs-lookup"><span data-stu-id="97f86-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="97f86-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="97f86-104">SYNTAX</span></span>

### <span data-ttu-id="97f86-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="97f86-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97f86-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="97f86-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97f86-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97f86-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeUser -InputObject <PSStackEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97f86-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97f86-108">DESCRIPTION</span></span>
<span data-ttu-id="97f86-109">Командлет **Set-AzStackEdgeUser** устанавливает новый пароль для пользователя на пограничном устройстве стопки.</span><span class="sxs-lookup"><span data-stu-id="97f86-109">The **Set-AzStackEdgeUser** cmdlet sets a new password for a user on the Stack Edge device.</span></span>

## <span data-ttu-id="97f86-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="97f86-110">EXAMPLES</span></span>

### <span data-ttu-id="97f86-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="97f86-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="97f86-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="97f86-112">PARAMETERS</span></span>

### <span data-ttu-id="97f86-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97f86-113">-AsJob</span></span>
<span data-ttu-id="97f86-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="97f86-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97f86-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97f86-115">-DefaultProfile</span></span>
<span data-ttu-id="97f86-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="97f86-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97f86-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="97f86-117">-DeviceName</span></span>
<span data-ttu-id="97f86-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="97f86-118">Device Name</span></span>

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

### <span data-ttu-id="97f86-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="97f86-119">-EncryptionKey</span></span>
<span data-ttu-id="97f86-120">Ключ шифрования на пограничном устройстве</span><span class="sxs-lookup"><span data-stu-id="97f86-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="97f86-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97f86-121">-InputObject</span></span>
<span data-ttu-id="97f86-122">Объект input</span><span class="sxs-lookup"><span data-stu-id="97f86-122">Input Object</span></span>

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

### <span data-ttu-id="97f86-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="97f86-123">-Name</span></span>
<span data-ttu-id="97f86-124">Действительно</span><span class="sxs-lookup"><span data-stu-id="97f86-124">Username</span></span>

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

### <span data-ttu-id="97f86-125">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="97f86-125">-Password</span></span>
<span data-ttu-id="97f86-126">Пароль, предоставление в качестве безопасной строки</span><span class="sxs-lookup"><span data-stu-id="97f86-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="97f86-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97f86-127">-ResourceGroupName</span></span>
<span data-ttu-id="97f86-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="97f86-128">Resource Group Name</span></span>

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

### <span data-ttu-id="97f86-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97f86-129">-ResourceId</span></span>
<span data-ttu-id="97f86-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="97f86-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="97f86-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97f86-131">-Confirm</span></span>
<span data-ttu-id="97f86-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="97f86-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97f86-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97f86-133">-WhatIf</span></span>
<span data-ttu-id="97f86-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="97f86-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97f86-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="97f86-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97f86-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97f86-136">CommonParameters</span></span>
<span data-ttu-id="97f86-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="97f86-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97f86-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97f86-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97f86-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="97f86-139">INPUTS</span></span>

### <span data-ttu-id="97f86-140">Ничего</span><span class="sxs-lookup"><span data-stu-id="97f86-140">None</span></span>

## <span data-ttu-id="97f86-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="97f86-141">OUTPUTS</span></span>

### <span data-ttu-id="97f86-142">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="97f86-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="97f86-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="97f86-143">NOTES</span></span>

## <span data-ttu-id="97f86-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97f86-144">RELATED LINKS</span></span>
