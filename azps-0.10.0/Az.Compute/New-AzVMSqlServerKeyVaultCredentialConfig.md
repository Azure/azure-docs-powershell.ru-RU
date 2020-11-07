---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: d9f732a40b61687d7970fdf24f9f9f0f841b2cc7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911457"
---
# <span data-ttu-id="794c4-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="794c4-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="794c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="794c4-102">SYNOPSIS</span></span>
<span data-ttu-id="794c4-103">Создает объект конфигурации для учетных данных хранилища ключей SQL Server на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="794c4-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="794c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="794c4-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="794c4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="794c4-105">DESCRIPTION</span></span>

## <span data-ttu-id="794c4-106">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="794c4-106">EXAMPLES</span></span>

## <span data-ttu-id="794c4-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="794c4-107">PARAMETERS</span></span>

### <span data-ttu-id="794c4-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="794c4-108">-AzureKeyVaultUrl</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="794c4-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="794c4-109">-CredentialName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="794c4-110">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="794c4-110">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="794c4-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="794c4-111">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="794c4-112">-Намерено</span><span class="sxs-lookup"><span data-stu-id="794c4-112">-ServicePrincipalName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="794c4-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="794c4-113">-ServicePrincipalSecret</span></span>
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="794c4-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="794c4-114">-Confirm</span></span>
<span data-ttu-id="794c4-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="794c4-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="794c4-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="794c4-116">-WhatIf</span></span>
<span data-ttu-id="794c4-117">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="794c4-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="794c4-118">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="794c4-118">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="794c4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="794c4-119">CommonParameters</span></span>
<span data-ttu-id="794c4-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="794c4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="794c4-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="794c4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="794c4-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="794c4-122">INPUTS</span></span>

### <span data-ttu-id="794c4-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="794c4-123">None</span></span>
<span data-ttu-id="794c4-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="794c4-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="794c4-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="794c4-125">OUTPUTS</span></span>

### <span data-ttu-id="794c4-126">Microsoft. Azure. Commands. COMPUTE. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="794c4-126">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="794c4-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="794c4-127">NOTES</span></span>

## <span data-ttu-id="794c4-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="794c4-128">RELATED LINKS</span></span>

