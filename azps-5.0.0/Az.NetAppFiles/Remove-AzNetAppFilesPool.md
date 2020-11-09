---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: 1ab6d38cc5401b4a7e813dafac933d6601a75acd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247284"
---
# <span data-ttu-id="4631a-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="4631a-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="4631a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4631a-102">SYNOPSIS</span></span>
<span data-ttu-id="4631a-103">Удаление пула файлов Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="4631a-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="4631a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4631a-104">SYNTAX</span></span>

### <span data-ttu-id="4631a-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4631a-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4631a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4631a-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4631a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4631a-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4631a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4631a-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4631a-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4631a-109">DESCRIPTION</span></span>
<span data-ttu-id="4631a-110">Командлет **Remove-AzNetAppFilesPool** УДАЛЯЕТ пул ANF.</span><span class="sxs-lookup"><span data-stu-id="4631a-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="4631a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4631a-111">EXAMPLES</span></span>

### <span data-ttu-id="4631a-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4631a-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="4631a-113">Эта команда удаляет пул ANF "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="4631a-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="4631a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4631a-114">PARAMETERS</span></span>

### <span data-ttu-id="4631a-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="4631a-115">-AccountName</span></span>
<span data-ttu-id="4631a-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="4631a-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4631a-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="4631a-117">-AccountObject</span></span>
<span data-ttu-id="4631a-118">Объект Account, содержащий пул, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="4631a-118">The account object containing the pool to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4631a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4631a-119">-DefaultProfile</span></span>
<span data-ttu-id="4631a-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4631a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4631a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4631a-121">-InputObject</span></span>
<span data-ttu-id="4631a-122">Объект пула, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="4631a-122">The pool object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4631a-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4631a-123">-Name</span></span>
<span data-ttu-id="4631a-124">Название пула ANF</span><span class="sxs-lookup"><span data-stu-id="4631a-124">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4631a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4631a-125">-PassThru</span></span>
<span data-ttu-id="4631a-126">Возвращает значение, указывающее, был ли указанный пул успешно удален</span><span class="sxs-lookup"><span data-stu-id="4631a-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="4631a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4631a-127">-ResourceGroupName</span></span>
<span data-ttu-id="4631a-128">Группа ресурсов в пуле ANF</span><span class="sxs-lookup"><span data-stu-id="4631a-128">The resource group of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4631a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4631a-129">-ResourceId</span></span>
<span data-ttu-id="4631a-130">Идентификатор ресурса пула ANF</span><span class="sxs-lookup"><span data-stu-id="4631a-130">The resource id of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4631a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4631a-131">-Confirm</span></span>
<span data-ttu-id="4631a-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4631a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4631a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4631a-133">-WhatIf</span></span>
<span data-ttu-id="4631a-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4631a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4631a-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4631a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4631a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4631a-136">CommonParameters</span></span>
<span data-ttu-id="4631a-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4631a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4631a-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4631a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4631a-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4631a-139">INPUTS</span></span>

### <span data-ttu-id="4631a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4631a-140">System.String</span></span>

### <span data-ttu-id="4631a-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="4631a-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="4631a-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="4631a-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="4631a-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4631a-143">OUTPUTS</span></span>

### <span data-ttu-id="4631a-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4631a-144">System.Boolean</span></span>

## <span data-ttu-id="4631a-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="4631a-145">NOTES</span></span>

## <span data-ttu-id="4631a-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4631a-146">RELATED LINKS</span></span>