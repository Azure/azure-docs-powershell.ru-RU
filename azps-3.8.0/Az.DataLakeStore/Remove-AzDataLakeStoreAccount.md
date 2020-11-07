---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
ms.openlocfilehash: 75af40b104bbf6ffa65211087572140a070b71e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912277"
---
# <span data-ttu-id="7561d-101">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7561d-101">Remove-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="7561d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7561d-102">SYNOPSIS</span></span>
<span data-ttu-id="7561d-103">Удаление учетной записи Data Lake Store без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="7561d-103">Deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="7561d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7561d-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7561d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7561d-105">DESCRIPTION</span></span>
<span data-ttu-id="7561d-106">Командлет **Remove-AzDataLakeStoreAccount** удаляет учетную запись Data Lake Store без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="7561d-106">The **Remove-AzDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="7561d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7561d-107">EXAMPLES</span></span>

### <span data-ttu-id="7561d-108">Пример 1: Удаление учетной записи Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="7561d-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="7561d-109">Эта команда удаляет учетную запись с именем ContosoADL из Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7561d-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="7561d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7561d-110">PARAMETERS</span></span>

### <span data-ttu-id="7561d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7561d-111">-DefaultProfile</span></span>
<span data-ttu-id="7561d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7561d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7561d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7561d-113">-Force</span></span>
<span data-ttu-id="7561d-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="7561d-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7561d-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7561d-115">-Name</span></span>
<span data-ttu-id="7561d-116">Указывает имя учетной записи, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="7561d-116">Specifies the name of the account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7561d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7561d-117">-PassThru</span></span>
<span data-ttu-id="7561d-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="7561d-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7561d-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7561d-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7561d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7561d-120">-ResourceGroupName</span></span>
<span data-ttu-id="7561d-121">Указывает группу ресурсов, которая содержит учетную запись, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="7561d-121">Specifies the resource group that contains the account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7561d-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7561d-122">-Confirm</span></span>
<span data-ttu-id="7561d-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7561d-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7561d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7561d-124">-WhatIf</span></span>
<span data-ttu-id="7561d-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7561d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7561d-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7561d-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7561d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7561d-127">CommonParameters</span></span>
<span data-ttu-id="7561d-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7561d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7561d-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7561d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7561d-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7561d-130">INPUTS</span></span>

### <span data-ttu-id="7561d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7561d-131">System.String</span></span>

## <span data-ttu-id="7561d-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7561d-132">OUTPUTS</span></span>

### <span data-ttu-id="7561d-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7561d-133">System.Boolean</span></span>

## <span data-ttu-id="7561d-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="7561d-134">NOTES</span></span>

## <span data-ttu-id="7561d-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7561d-135">RELATED LINKS</span></span>

[<span data-ttu-id="7561d-136">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7561d-136">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="7561d-137">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7561d-137">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="7561d-138">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7561d-138">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="7561d-139">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7561d-139">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


