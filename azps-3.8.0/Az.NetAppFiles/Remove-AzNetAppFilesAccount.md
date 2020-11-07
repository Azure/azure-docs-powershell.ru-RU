---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: de0f71a91ec4445ae4be58e904e58eb3a97cb9a0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911745"
---
# <span data-ttu-id="237cf-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="237cf-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="237cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="237cf-102">SYNOPSIS</span></span>
<span data-ttu-id="237cf-103">Удаление учетной записи NetApp файлы Azure (ANF).</span><span class="sxs-lookup"><span data-stu-id="237cf-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="237cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="237cf-104">SYNTAX</span></span>

### <span data-ttu-id="237cf-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="237cf-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="237cf-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="237cf-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="237cf-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="237cf-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="237cf-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="237cf-108">DESCRIPTION</span></span>
<span data-ttu-id="237cf-109">Командлет **Remove-AzNetAppFilesAccount** удаляет учетную запись ANF.</span><span class="sxs-lookup"><span data-stu-id="237cf-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="237cf-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="237cf-110">EXAMPLES</span></span>

### <span data-ttu-id="237cf-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="237cf-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="237cf-112">Эта команда удаляет учетную запись ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="237cf-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="237cf-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="237cf-113">PARAMETERS</span></span>

### <span data-ttu-id="237cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="237cf-114">-DefaultProfile</span></span>
<span data-ttu-id="237cf-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="237cf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="237cf-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="237cf-116">-InputObject</span></span>
<span data-ttu-id="237cf-117">Удаляемый объект учетной записи</span><span class="sxs-lookup"><span data-stu-id="237cf-117">The account object to remove</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="237cf-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="237cf-118">-Name</span></span>
<span data-ttu-id="237cf-119">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="237cf-119">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="237cf-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="237cf-120">-PassThru</span></span>
<span data-ttu-id="237cf-121">Возвращает значение, указывающее, успешно ли была удалена указанная учетная запись</span><span class="sxs-lookup"><span data-stu-id="237cf-121">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="237cf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="237cf-122">-ResourceGroupName</span></span>
<span data-ttu-id="237cf-123">Группа ресурсов для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="237cf-123">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="237cf-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="237cf-124">-ResourceId</span></span>
<span data-ttu-id="237cf-125">Идентификатор ресурса для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="237cf-125">The resource id of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="237cf-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="237cf-126">-Confirm</span></span>
<span data-ttu-id="237cf-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="237cf-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="237cf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="237cf-128">-WhatIf</span></span>
<span data-ttu-id="237cf-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="237cf-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="237cf-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="237cf-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="237cf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="237cf-131">CommonParameters</span></span>
<span data-ttu-id="237cf-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="237cf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="237cf-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="237cf-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="237cf-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="237cf-134">INPUTS</span></span>

### <span data-ttu-id="237cf-135">System. String</span><span class="sxs-lookup"><span data-stu-id="237cf-135">System.String</span></span>

### <span data-ttu-id="237cf-136">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="237cf-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="237cf-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="237cf-137">OUTPUTS</span></span>

### <span data-ttu-id="237cf-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="237cf-138">System.Boolean</span></span>

## <span data-ttu-id="237cf-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="237cf-139">NOTES</span></span>

## <span data-ttu-id="237cf-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="237cf-140">RELATED LINKS</span></span>
