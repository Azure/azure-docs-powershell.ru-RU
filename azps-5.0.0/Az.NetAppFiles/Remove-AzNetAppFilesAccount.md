---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: 5f6e2421a20cb7aaf044d3abfbbddf7f5c72b37e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245715"
---
# <span data-ttu-id="bfc08-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="bfc08-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="bfc08-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bfc08-102">SYNOPSIS</span></span>
<span data-ttu-id="bfc08-103">Удаление учетной записи NetApp файлы Azure (ANF).</span><span class="sxs-lookup"><span data-stu-id="bfc08-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="bfc08-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bfc08-104">SYNTAX</span></span>

### <span data-ttu-id="bfc08-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bfc08-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc08-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfc08-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc08-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfc08-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfc08-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfc08-108">DESCRIPTION</span></span>
<span data-ttu-id="bfc08-109">Командлет **Remove-AzNetAppFilesAccount** удаляет учетную запись ANF.</span><span class="sxs-lookup"><span data-stu-id="bfc08-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="bfc08-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bfc08-110">EXAMPLES</span></span>

### <span data-ttu-id="bfc08-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bfc08-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="bfc08-112">Эта команда удаляет учетную запись ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="bfc08-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="bfc08-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bfc08-113">PARAMETERS</span></span>

### <span data-ttu-id="bfc08-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfc08-114">-DefaultProfile</span></span>
<span data-ttu-id="bfc08-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bfc08-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfc08-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bfc08-116">-InputObject</span></span>
<span data-ttu-id="bfc08-117">Удаляемый объект учетной записи</span><span class="sxs-lookup"><span data-stu-id="bfc08-117">The account object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfc08-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bfc08-118">-Name</span></span>
<span data-ttu-id="bfc08-119">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="bfc08-119">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc08-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bfc08-120">-PassThru</span></span>
<span data-ttu-id="bfc08-121">Возвращает значение, указывающее, успешно ли была удалена указанная учетная запись</span><span class="sxs-lookup"><span data-stu-id="bfc08-121">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="bfc08-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfc08-122">-ResourceGroupName</span></span>
<span data-ttu-id="bfc08-123">Группа ресурсов для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="bfc08-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="bfc08-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfc08-124">-ResourceId</span></span>
<span data-ttu-id="bfc08-125">Идентификатор ресурса для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="bfc08-125">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="bfc08-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfc08-126">-Confirm</span></span>
<span data-ttu-id="bfc08-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bfc08-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfc08-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfc08-128">-WhatIf</span></span>
<span data-ttu-id="bfc08-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bfc08-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfc08-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bfc08-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfc08-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfc08-131">CommonParameters</span></span>
<span data-ttu-id="bfc08-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bfc08-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfc08-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bfc08-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfc08-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bfc08-134">INPUTS</span></span>

### <span data-ttu-id="bfc08-135">System. String</span><span class="sxs-lookup"><span data-stu-id="bfc08-135">System.String</span></span>

### <span data-ttu-id="bfc08-136">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="bfc08-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="bfc08-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfc08-137">OUTPUTS</span></span>

### <span data-ttu-id="bfc08-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bfc08-138">System.Boolean</span></span>

## <span data-ttu-id="bfc08-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="bfc08-139">NOTES</span></span>

## <span data-ttu-id="bfc08-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bfc08-140">RELATED LINKS</span></span>
