---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
ms.openlocfilehash: c344d5ac901e45c92c04a23cee252b1f747d4a83
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910426"
---
# <span data-ttu-id="62295-101">Set-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="62295-101">Set-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="62295-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62295-102">SYNOPSIS</span></span>
<span data-ttu-id="62295-103">Установка нового пароля для пользователя на устройстве.</span><span class="sxs-lookup"><span data-stu-id="62295-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="62295-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62295-104">SYNTAX</span></span>

### <span data-ttu-id="62295-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="62295-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62295-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62295-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62295-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62295-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -InputObject <PSDataBoxEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62295-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62295-108">DESCRIPTION</span></span>
<span data-ttu-id="62295-109">Командлет **Set-AzDataBoxEdgeUser** устанавливает новый пароль для пользователя на пограничном устройстве поля данных.</span><span class="sxs-lookup"><span data-stu-id="62295-109">The **Set-AzDataBoxEdgeUser** cmdlet sets a new password for a user on the Data Box Edge device.</span></span>

## <span data-ttu-id="62295-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62295-110">EXAMPLES</span></span>

### <span data-ttu-id="62295-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="62295-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="62295-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62295-112">PARAMETERS</span></span>

### <span data-ttu-id="62295-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62295-113">-AsJob</span></span>
<span data-ttu-id="62295-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="62295-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62295-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62295-115">-DefaultProfile</span></span>
<span data-ttu-id="62295-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62295-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62295-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="62295-117">-DeviceName</span></span>
<span data-ttu-id="62295-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="62295-118">Device Name</span></span>

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

### <span data-ttu-id="62295-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="62295-119">-EncryptionKey</span></span>
<span data-ttu-id="62295-120">Ключ шифрования на пограничном устройстве</span><span class="sxs-lookup"><span data-stu-id="62295-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="62295-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62295-121">-InputObject</span></span>
<span data-ttu-id="62295-122">Объект input</span><span class="sxs-lookup"><span data-stu-id="62295-122">Input Object</span></span>

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

### <span data-ttu-id="62295-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="62295-123">-Name</span></span>
<span data-ttu-id="62295-124">Действительно</span><span class="sxs-lookup"><span data-stu-id="62295-124">Username</span></span>

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

### <span data-ttu-id="62295-125">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="62295-125">-Password</span></span>
<span data-ttu-id="62295-126">Пароль, предоставление в качестве безопасной строки</span><span class="sxs-lookup"><span data-stu-id="62295-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="62295-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62295-127">-ResourceGroupName</span></span>
<span data-ttu-id="62295-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="62295-128">Resource Group Name</span></span>

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

### <span data-ttu-id="62295-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62295-129">-ResourceId</span></span>
<span data-ttu-id="62295-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="62295-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="62295-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62295-131">-Confirm</span></span>
<span data-ttu-id="62295-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="62295-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62295-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62295-133">-WhatIf</span></span>
<span data-ttu-id="62295-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="62295-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62295-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="62295-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62295-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62295-136">CommonParameters</span></span>
<span data-ttu-id="62295-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62295-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62295-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62295-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62295-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62295-139">INPUTS</span></span>

### <span data-ttu-id="62295-140">Ничего</span><span class="sxs-lookup"><span data-stu-id="62295-140">None</span></span>

## <span data-ttu-id="62295-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62295-141">OUTPUTS</span></span>

### <span data-ttu-id="62295-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="62295-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="62295-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="62295-143">NOTES</span></span>

## <span data-ttu-id="62295-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62295-144">RELATED LINKS</span></span>
